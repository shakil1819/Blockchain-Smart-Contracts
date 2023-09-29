# Validation & Test (Part 1) (BallotV3 Demo)

---
![[index_4.mp4]]

Module three, lesson three: Problem-specific Validation and Testing. The learning objectives of this lesson are: explain the concept of reverting a transaction based on problem-specific validation and using a revert declaration, apply the concepts of function modifier; require; and assert. In this lesson, we will show the execution after modifying ballotversion2.sol using solidity-specific declarations and error handlers. Modifier, require and assert. Solidity features a function revert that results in state-reverting exception. This exception handling will undo all the changes made to the state in the current call and reverses the transaction and also flags an error to the caller. We will introduce a function modifier with the required stage as a parameter. First, we'll add the modifier to the function header. We'll add the modifier with the parameter, stage required stage. Let us review the code with the modifier added. Let us execute the ballot version three with all these improvement. Every now and then when you're working with Remix, it's good to refresh so that you get new account numbers and the space is clean, and so on. I've done that. And so you can see that I've been working on several of them, so they're all open here, and I'm going to choose the version three, ballot version three. And, here, you can see that I have, in the last one, I did not use any modifiers. Here, this one illustrates modifiers require assert, and all the gatekeeper elements that we discussed in the lectures. Okay, so let's go back. This is ballot version three. I have the regular struct for voter, struct for proposal, enum for stage, address for the chairperson, mapping the address to the voters in the proposal array. So, these are all quite familiar to you by now. And you can see how beneficial incremental development is. You take the base contract and put the essentials there and keep adding to it. That helps in better development and a good design. And now you also have the time element and start time, and we see some new things here. I have a single modifier, validStage. Instead of checking the stage inside using if-else statement, which requires the transaction to be executed inside the function, we can prevent that from happening right outside the function using the modifier as you can see here. So, let's look at the modifier. Modifier validStage has a parameters stage, and so every time you want to execute a function, register, vote, or winningProposal, we make sure we are in the right stage to do that based on the elapsed time. Once again, I given a very low elapsed time for the demo purposes. In reality, it's going to be higher. Let's review the code one last time before we go into run. This is the constructor. It has the same name as the ballot, and it requires the number of proposals as a parameter. Chairperson is the sender of this message, and we have designated chairperson voters two that I've been mentioning in the last few demos. And number of proposals is what you were passing in as parameters. For the sake of the demo, we are setting it at three. And more importantly, we are setting the stage to be the registration stage. We are finished with the init stage. Now, we are moving into registration stage and the start time is set as now. And when you go into the register, here, I have here the valid stage modifier specified as one of the modifiers for the function. Function, register, parameters, public is a visibility modifier. ValidStage is a access modifier, custom access modifier, that we defined. And we also have a parameter for that modifier. So at the outset, at the head of the function, we can see clearly, this function will not be executed if validStage is not reg. Okay, that's the beauty of the modifier. And once you go inside, I replace the if statement, the regular programmatic statement with that modifier. So, this was the previous version. Now, we made it at the header so the modifier stops it from going into the function itself. We were checking it inside the function, now at the header of the function, we're checking it. And then, the rest of the things are the regular code, except for the last one, where I'm checking if the elapsed time is over for the registration. If so, I'm moving on to the stage, vote, by setting the stage to the next stage. And the vote function. Here again, I have public, which is a visibility modifier, and I have an access modifier in validStage. As you can see, that was stage registration for registration. This has to be Stage.Vote in order for you to vote. Once again, I'm also keeping the if statement from last version so that you can see what replaced this. This if statement was replaced by the modifier, validStage, Stage.Vote. That is what we defined before. And inside, I have the regular code for counting the votes, and registering the votes, and other things. And at the end, if the elapsed time for the voting phase has moved, I set the stage to the done stage. I also have votingCompleted. This is an event, okay? We'll talk about that later. And I have a winningProposal that also executes only if the stage is done. Otherwise, it doesn't execute. It simply returns false or error so that we know that winning stage has not been arrived at, and we don't have any valid results yet.