Metacrafters ATM
Welcome to the Metacrafters ATM! This application allows users to deposit and withdraw ETH using MetaMask.

Getting Started
To get started with the Metacrafters ATM, follow these steps:

Clone this repository to your local machine.
Install dependencies by running npm install.
Start the development server with npm start.
Open the application in your web browser.

Usage
Connect your MetaMask wallet.
View your account balance.
Input the amount to deposit or withdraw.
Click the corresponding button to complete the transaction.

Technologies Used
-React
-ethers.js
-MetaMask

State Management
The component uses React's useState hook to manage state variables such as ethWallet, account, atm, balance, and amount. These variables are used to keep track of the user's MetaMask wallet, connected account, ATM contract instance, account balance, and transaction amount, respectively.
Ethereum Integration
The component imports ethers from the ethers.js library and atm_abi from a JSON file containing the ABI (Application Binary Interface) of the ATM smart contract.
Wallet Connection
The getWallet function is called when the component mounts to check if MetaMask is installed and available in the browser. If MetaMask is detected, the user's account is requested, and handleAccount is called to update the account state.

The connectAccount function is triggered when the user clicks the "Connect" button. It requests access to the user's MetaMask account and calls handleAccount to update the account state.

Contract Interaction
The getATMContract function initializes an instance of the ATM smart contract using ethers.Contract. It requires the provider from the user's MetaMask wallet, a signer, and the contract's address and ABI.

The getBalance function retrieves the user's account balance from the ATM smart contract and updates the balance state.

Transaction Handling
The deposit function allows users to deposit ETH into the ATM. It calls the deposit method of the ATM smart contract, passing the specified amount as a parameter.

The withdraw function allows users to withdraw ETH from the ATM. Similar to deposit, it calls the withdraw method of the ATM smart contract.

User Interface
The initUser function renders different UI elements based on the user's MetaMask connection status and account balance.

When the component renders, the getWallet function is called to initialize MetaMask integration.

Styling
The component uses Tailwind CSS classes for styling elements such as buttons, inputs, and text.


