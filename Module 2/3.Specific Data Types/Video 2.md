# Specific Data Types (Part 2) (Coin Demo cont.)

![[index_1.mp4]]

[MUSIC] We looked at the structure of coin,
now let's look at it in operation. And let's mint some coins and
send it between accounts. Compile, you have a clean compile. Run, and I'm going to create. And that deploys a smart contract
with public data and public methods. And I'm going to check
the balance of the mentor. None of that column should have
any coins because we just started. So I'm going to say balance and
it's going to be zero. If you check the other accounts also,
it would be zero, and I'm going to mint some coins for
the minter, the creator of the. I'm going to say 2,000, mint, and
we have here, let me go back and check if we have 2,000. Now I'm going to go back
to another account, copy the account address,
and put it in the send. Make sure it is copied and
it's the right address. And I'm going to send 600
of the coin that I created from the minter's account
to the new account. And let's go back here, let's go
back here, and see whether we have that particular account has
that 600 coins that we sent. So here we have balance 600. So we minted 2,000 coins,
we sent 600 coins. And now I'm going to go back
here to the minter's account. Minter's account should show 1,400 because
it has sent 600 of them, balance, yes. We know that it's nicely balanced. In summary, it is impossible to enumerate every
possible language element of solidity. However, in this lesson we've established
a method you can follow to learn and practice new constructs for
building smart contract. We learned the concept of address,
mapping, and message, and applied these to analyze
a simple contract coin. One more thing. Always design before you code. We did that with the class
diagram of the coin example. And explore the coding examples by
uploading them to the remix and map.
