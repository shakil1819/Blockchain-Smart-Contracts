![[Module 2/5.Access Modifiers & Applications/attachments/index_3.mp4]]

```
On completion of this lesson, you will be able to explain
usage of function modifiers, explain the use of require
clause for input validation, illustrate the assert declaration for post-condition checking, discuss reverting a transaction
and reward function. The main intent of smart contract transaction
is to execute a function. However, smart contracts
often require control over who are what
can execute the function, at what time a function
needs to be executed, what are the precondition to be met before getting
access to the function? It's a good practice to validate input values
to the function to avoid unnecessary execution
and waste of gas. If there are any errors found during
the input validation, these have to be
handled appropriately. At the end of
the function execution, you may want to assert that
certain conditions are met to ensure the integrity
of the smart contract. Let's begin with an important feature of
solidity, modifiers. They can address some of
the concerns just mentioned. Modifiers can change
the behavior of a function. That's why this feature is
referred to as a modifier. It is also known as a function modifier
since it is specified at the entry to a function and executed before the execution
of the function begins. You can think of a modifier as a gatekeeper
protecting a function. A modifier typically
checks a condition using a require and if
the condition failed, the transaction that call the function can be reverted
using the revert function. This will completely reject the transaction and revert
all its state changes. There'll be no recording
on the blockchain. Let's understand the
modifier and require clauses using the ballot
smart contract functions. We'll add a modifier onlyBy(chairperson) to
the register function. Will do that by the steps. Define modifier for the
clause onlyBy(chairperson). Adding a special
notation underscore semicolon to
the modifier definition that includes the function. Using the modifier clause
in the function header. Step 1 is a definition
of the modifier onlyBy, only the chairperson who created the smart contract valid to
register any new orders. Step 2, shows how to make the modifier include
a place holder for any function. Step 3, use the modifier clause in the header of
the function definition. Now, let's change
the existing if statement of the ballot smart contract such that it reverse the transaction on
input validation failure. We don't need to waste blockchain resources for
a failed transaction. Now, we'll illustrate
assert using a function payoff that
computes and pays off bets. It is preferable that the
assert not fail and that it requires checking
the balance after every payoff in the above case. We are making sure bank
has the reserves of $10,000 after all the payoffs. Under normal circumstance,
assert should not fail. This is more for
handling an anomalous, faulty or malicious condition. In this case, the
exceptional condition is that bank balance somehow
dipped below the reserves. The picture summarizes
all the features we discussed. Modifiers and error handlers, and where they are
typically used. The rules, laws, policies, and governance conditions
are coded as modifiers. You can use the modifiers as gatekeepers for the functions. If your transaction to
invoke the function does not meet the condition specified at the header
of the function, your transaction
will be reverted. Will not be recorded
in the block chain. Modifiers can be used
to validate rules outside the function such as describing the opening
of the lesson, who has access to the function, at what time, and
what condition, etc. Once the screening
conditions are satisfied, input validation can
be carried out inside the function using
require declaration statement. In this case, also the transaction will be
reverted on failed validation. This is done before
the execution of the function. There are anomalous
faulty malicious code that may result in unexpected
situations or exception. These can be caught usually at the end of the function
or sometimes within the function using
assert declarative statement, and the entire
transaction including the function execution and the state change
will be reverted. Here is an example of
an online digital media bazaar. Input condition as specified by a modifier is atLeast5Sellers. This enforces the condition that there should be
atLeast5Sellers with their products before a buyer initiates a buy message
through a transaction. This is a global condition
for all buyers. So, it is appropriate
to install it using a modifier
declarative statement. Once there are enough sellers, a buyer can buy. Inside the function, we
validate if the buyer has enough money to buy
the specific item requested. If not, the transaction
is reverted. When the validation is satisfied, money is transferred
to the seller, item is transferred to the buyer. We have a simple
assert declaration at the end that the bought item should have been transferred. After all, it's a digital item. This simply reached only
if the item has not been transferred and could not be transferred due to
exception reason. This provides a simple example of concepts learned
in this lesson. In summary, function modifiers along with state reverting
functions of revert, required, and assert,
collectively supported robust error handling-approach
for a smart contract. These declarative
features can be used to perform formal
verification and static analysis of
a smart contract to make sure it implements the intent
of a smart contract.
```