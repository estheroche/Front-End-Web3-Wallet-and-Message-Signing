

# Calculator Contract. 

Let's break down the code step-by-step:



1. Contract Definition and State Variables:

   - `address public owner;`: This variable stores the address of the contract owner. It is publicly accessible.

   - `uint public stateValue;`: This variable stores the current state value of the contract. It is also publicly accessible.

2. Constructor:

   - `constructor () { owner = msg.sender; }`: This function is called when the contract is deployed. It sets the owner variable to the address of the sender, which is the person deploying the contract.

3. Modifiers:

    - `modifier onlyOwner() { require(msg.sender == owner,` "Only the contract owner can call this function"); _; }: This modifier is used to restrict the access of certain functions to the contract owner. It checks if the sender of the function call is the same as the owner variable. If not, it throws an error.
   -  _;: This symbol represents the body of the function that the modifier is applied to. It is placed after the modifier's code to ensure that the function continues to execute if the modifier's requirements are met.

4. Functions:

   -  `setState(uint256 _newValue) public onlyOwner:` This function allows the contract owner to set the stateValue to a new value. It takes a single parameter, `_newValue,` which is the new value to be set. This function is protected by the `onlyOwner` modifier, which ensures that only the contract owner can call it.
   - `multiplyState(uint256 _multiplier) public:` This function multiplies the stateValue by a given multiplier. It takes a single parameter, `_multiplier`, which is the multiplier to be used.
   - `divideState(uint256 _divisor) public:` This function divides the stateValue by a given divisor. It takes a single parameter, `_divisor`, which is the divisor to be used. This function includes a require statement to check if the divisor is not zero. Dividing by zero is not allowed as it would cause an error.

In summary, this contract is a simple calculator that allows the contract owner to set the state value, multiply it, and divide it. It ensures data security by using modifiers to restrict access to certain functions to the contract owner.


# Front-End 

- This DAPP used tailwindCSS for styling.
- Its a React plus Vite App


# contract Address

[0xc63A24f469E1eFe196968D9126a289f3b462E8F3](https://sepolia.etherscan.io/address/0xc63A24f469E1eFe196968D9126a289f3b462E8F3)


# Front-end Deployment to vercel link

https://front-end-web3-wallet-and-message-signing-tj2e.vercel.app/






