# Time Elements (Part 2) (BallotV2 Demo)
---
![[Module 3/1.Time Elements/attachments/index.mp4]]



This is Ballot version 2. Version 2 has a struct for Voter,
it has a struct for Proposal. And has something new here, enum stage, that defines init reg vote and
done stages for the smart contract. And the variable stage is defined
to be of this enum stage type, and it has been initialized to the Init stage. Actually Init is 0, Reg is 1,
Vote is coded as 2, Done is coded as 3. Remember that when we are looking at
the outputs in the web interface. Address chairperson, chairperson is the
only person who can register other voters. Mapping, address is mapped to the voter
struct, and we have a Proposal and an array of proposals that has each
one of the structs for the Proposal. That is just one data field
called uint voteCount. And we also define the time
element uint startTime. These are some of the things that are new. We have the usual constructor, and the constructor has two more lines besides
the previous code that is defining the stage to be reg, and
also start startTime to be now. So, it initiates the registration stage. And the register function happens
only if the stage happens to be reg, otherwise it simply returns. This is a new feature that we have
added to the Ballot version 2, okay? It used to be just this code,
now we have added one more check in the validation at the beginning
of the function, okay. And that is based on the enum
stage that we've created. The same way you can vote only
if the stage happens to be, I'm going down here and you can see
that if you can vote only if the stage happens to be vote,
otherwise the function simply returns. And finally, and the winning proposal returns something
useful only if the stage is done. Otherwise, it doesn't even
go through computing. This winning proposal doesn't even
execute if the stage is not done. All right, so
we enforce some checkpoints here, some validations here from
the first version of the Ballot. So let's execute it and see it running. I'm going to compile, it's already
compiled, but anyway compile again. JavaScript, and I am going to change
that address like you can see that we have several addresses and
I am going to change that address to be the chairperson's address,
that is arbitrarily decided. But I would like to have the ca3 to be
chairperson's address every time, and I am going to create it once again
with just three proposals, Create, and you can see the interface here, okay. So I have here vote register,
and I also put the stage, stage also came up here, since I define
the stage variable to be public. It is also coming and showing in the web
interface, since it's a public variable, getters are automatically set for
it, and so stages also here, so you can view the stage also. All right, so
first thing is we need to register. So the chairperson is here sending,
ready to send the message. And I want to find out who
is to be registered first. This is the second person, this the first
person who is to be registered and so I'm going to copy that address and
then throw it in here. [COUGH] And remember,
remix requires it within quotes. And I have to go back here and create or show the chairperson as the sender
of this register message. Nobody else except
the chairperson can register. So I set the Account address who's
sending the register function to be the chairperson. And then this is the person to be
registered, and I say, register. Okay, now that person is registered so
we have two people. One, the chairperson, and one more. I’m going to show you registration for
one more person, let's see. I have here one more person,
copy, and I can copy it here. And again,
I want to emphasize that this is going to be within code, and I just want to make
sure that I have a different address. You can see it's 4b and I have to change
the sender to be the chairperson and then I'm going to register. We've registered two people here. Okay, let's register one more. 583, I'm going to copy, so
you got the idea here right now, and this has to be within codes, and
you can use a Ctrl+V to copy that, you could use copy and
paste if you're a copy and paste person. Let's see, Ctrl+V,
I have it here, all right. And so, I go back to the chairperson,
and register. In this case I registered
three people here. Okay, and the stage is two now,
okay, so stage is two, that means elapsed time is ready to go and
we can vote. So I'm going to go back
to the chairperson. Chairperson votes for let's say 1, okay that means two votes
are registered for 1 okay. And I'm going to do only one more vote
because for the sake of I don't want copy. So I"m just going to,
the second person votes for 2. Okay, the regular voter votes for 2. All right, and
now let's look at the stage. Okay 3, it's ready to go, it's all done. So the winning proposal is 1, because
remember, the chairperson voted for 1, the single voter voted for 2,
the chairperson weighted is 2. So the winning proposal is one, all right? You can also keep checking the stages,
every now and then, whether you are in the right stage. In this case I made the stage
time to be very small so I could go through it quickly. But in reality, in a real smart
contract it can be few days that it be allowed to vote, and so on. Right, that is the end of Ballot 2.