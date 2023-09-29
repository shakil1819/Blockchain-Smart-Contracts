1. How are time elements added to BasicBallot contract we discussed earlier?
   - Using "now" variable along with 

2. In BallotWithStages.sol, how are the stages validated in register and vote functions?
   - Using if and require statements

3. Compile and create BallotWithStages.sol. Immediately try and vote. What is the status of the transaction?
   - Transaction mined and execution succeds

4. Time variable "now" does not provide the real current time. True or False?
   - True

5. In BallotWithModifier.sol, where is the condition about the stages defined?
   - Inside the modifier

6. Assert statement in the winningProposal method of BallotWithModifier.sol makes sure that the function does not return a value if nobody voted. True or False?
   - True

7. Compile and create BallotWithModifier.sol. Immediately try and vote. What is the status of the transaction?
   - Transaction mined and execution fails

8. Even though we have specified only tens of seconds (30 and 60 seconds) as the stage time, the stage time or duration in a real-life application could be longer. True or False?
   - True

9. What stage does the contract have to be in for winningProposal to produce a result?
   - 3 (Done Stage)

10. In BallotWithModifiers.sol, how is the end of the voting stage indicated to the other applications?
    - Using the event votingCompleted

![[Pasted image 20230930005243.png]]

