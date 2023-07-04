### Solidity: Structure
![[Module 2/1.Structure/attachments/index.mp4]]


| Timestamp | Transcript                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 0:00      | [MUSIC] Welcome to the second module, Solidity, the second course in the blockchain specialization. We will use Solidity as a high level language for implementing a smart contract. Solidity is a high level language that is a combination of JavaScript, Java, and C++. It is specially designed to write smart contracts and to target the Ethereum Virtual Machine.                                                                                                               |
| 0:30      | Recall from our course one that the format of a smart contract is like the class definition in the object-oriented programming style.                                                                          |
| 0:42      | In this course, we learn the important features of Solidity and the development of a smart contract through two specific problems. To create and view the smart contracts, we'll use Remix Web IDE for Solidity. There are many IDEs available. We chosen to use Remix, which provides not only a compiler, but also a runtime to test a smart contract you will design. Most of all, it works without any software insulation on your computer. Remix supports free runtime test environments, JavaScript VM, Injected Web3, like Metamask, and Web3 Provider, for example, your locally running Ethereum node. |
| 1:31      | We'll use only JavaScript environment for this module.                                                                                     |
| 1:35      | Our goal is to master the Solidity basics in this course. In the next module, we'll explore our approaches to deploying and invoking a smart contract on a test blockchain based on Injected Web3 and Web3 Provider. [MUSIC] Recall that we examined the structure of a simple smart contract in the last lesson.                                                                                                                                                                                           |
| 2:03      | Here is a more detailed structure of a smart contract. After this lesson, you will be able to discuss the elements of Solidity, a high level language for writing smart contract. Illustrate data types, and data structures, and functions, enum, modifiers, and events using Solidity code.                                                                                                                                                    |
| 2:24      | Apply these concepts to design, develop, deploy, and test a smart contract.                                                                 |
| 2:29      | Here is a more detailed structure of a smart contract.                                                                                     |
| 2:33      | Data or state variables, functions, there are several types of functions allowed. Constructor, default or user-specified, only one, meaning it cannot be overloaded. Fallback function, there's a powerful feature of an anonymous function                                                                                                  |
| 2:53      | that we'll discuss in later courses.                                                                                                      |
| 2:58      | View functions, pure functions, no state change, it computes under terms of value, example math functions. Public functions, accessible from outside, two transactions, state changes recorded on the blockchain. Private function, accessible only with the current contract.                                                                                                                                             |
| 3:19      | Internal function, accessible inside the current contract and inherited contracts. External functions can be accessed only from outside the smart contract. User-defined types in struct and enums. Modifiers and, finally, events.                                                                                                                       |
| 3:41      | Besides its explicit content, a smart contract can also inherit from another smart contract, as shown in the following example.                                                                              |
| 3:51      | Here standard policies contract defines basic policies that apply to all states, which is inherited by NYPolicies, smart contract, where more policies can be added.                                                                                                                        |
| 4:09      | Now, we step into the smart contract and look at the function definition.                                                                   |
| 4:14      | Function definitions are similar to functions in any other high-level language. Function header, followed by the code, within curly brackets. Function code contains the local data and statements to process the data and return the results of processing. Function header can be as simple as an anonymous noname function to a complex function header loaded with a lot of details. Here is more explanation of each of the items of the function header. |
| 4:48      | Function is a keyword at the beginning of all functions. Parameters are any number of pairs type identifier, example, UInt count. returnParameters, return values can be specified as pair type identifier or just type. When only type is specified, it has to be explicitly returned using a return statement.                                                                                                                     |
| 5:16      | If type and identifier are specified in the return statement, any state chain that happens to the identifier within the function is automatically returned.                                                                                                                     |
| 5:29      | Any number of values can be returned, unlike common programming languages that allow only one return value. For example, multiple variables, age and gender, can be assigned return values from a function getAgeGender.                                                                                                                            |
| 5:47      | In summary, a smart contract for Ethereum can be specified using Solidity defined structure and functions. A variety of function types are provided for expressing smart contract operations. A smart contract in Solidity can inherit its attribute and functionality from another smart contract.                                                                             |