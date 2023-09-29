# Validation & Test (Part 2) (BallotV4 Demo)

---
![[Module 3/2.Validation and Test/attachments/index.mp4]]


Here we see [COUGH] a familiar ballot
contract with a few more items added. We have a modifier, and also we have
the time and stage elements of that. [COUGH] You're allowed to vote
only at certain times and you're allowed to only
register at certain times. You can find out the winning
proposal only at a certain stage. Okay [COUGH] I'm going to compile and
it's already compiled. Run, and it's time dependent. I'm going to go through a little faster. And here I have all the public
variables and methods. And I'm going to register just one person. And I just want to make sure that
I'm in the stage 2 register. So I'm going to copy that address [COUGH]
and you can see that it is being copied. And I have to go back
to the base address or the address of the owner
of the smart contract. I register, it goes through fine. Now I'm looking at the stage,
it is not changed. So I'm going to register one more person,
and copy [COUGH] and put it in there. And I'm going to go back to
the chairperson and register. Two people have been registered. So I'm in the stage, and now I can vote. So chairperson votes for 2. And I'm going to go back to one
of the addresses and vote for 1. Understand that the chairperson
has voted for 2. Now I go back to stage and,
okay, so all right. So now I'm going to go back to
the third person and vote for 2 again. So we have a lot of votes for 2. We are in stage, it should be 2. Okay, I'm looking at the winning proposal,
and it's 2. And we've completed a simple demo. Let me just go back and
see whether we can show a revert here. Because we are not in the right stage,
so I'm going to now vote for [COUGH] 1. And you can see that it reverted
because we are not anymore in the reverting stages, and
we are not anymore in the voting stages. I'm going to register it reverted because
we are not anymore in the register state. We are only in the final
stage of winning proposal. And that is the demo of
the ballot revert in case you are not in the right timeframe and
you are not in the right stage terminal. Please do explore this on your own so
to understand the various components here. Observe that we have given the time
duration for the registration and voting processes one minutes so that we
can complete the testing in a finite time. In reality,
these times will be replaced by actual duration of each of
the registration and voting activities. Consider this issue. The base mark contract for
the ballot given in solidity documentation will indicate proposal zero as
the winning proposal even if no voters or votes are registered. That is by default
the proposal that came first, numbered zero,
will be chosen as the winning proposal. This is not intended. How are we going to address this issue? We will address it by
using an assert clause at the end of the function
winningProposal. Next, we'll look at interfacing
with client applications.