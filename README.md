# SOLIDITY Final

In this project module, I was able to create my first token 

## Description

* In this project,my contract has public variables that store the details about my coin (Token Name- Fast&Furious, Token Abbrv-FNF, Total Supply-5)

* My contract has a mapping of addresses to balances (address => uint)

* It has a mint function that takes two parameters: an address and a value. 
* The function then increases the total supply by that number and increases the balance of the address by that amount.
* The contract has a burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the address.
* Lastly, the burn function has conditionals to make sure the balance of account is greater than or equal to the amount that is supposed to be burned.
## Getting Started

### Installing the code

You can run the code on remix or download it locally on your computer.

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., final.sol). Copy and paste the following code into the file:

```javascript
pragma solidity 0.8.9;

contract MyToken {

    // public variables here
    string public tokenname="Fast&Furious";
    string public tokenabbrv="FNF";
    uint public totalsupply=5;
    // mapping variable here
    mapping(address => uint)public balance;
    // mint function
    function mint(address account, uint  mint_amt)public {
      totalsupply += mint_amt;
      balance[account] += mint_amt;
   }
    // burn function
   function burn(address account, uint burn_amt)public {
      if(balance[account]>= burn_amt){
        totalsupply -= burn_amt;
        balance[account] -= burn_amt;
      }
     }
  }

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.9" (or another compatible version), and then click on the "Compile final.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "final" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it . 

Click mint to call the mint function.

Click burn to call the burn function.

Click balance to check the balance of the entered account address.
## Authors

Francis MS

@francismariasharon@gmail.com

## License

This project is licensed under the [MIT] License - see the LICENSE.md file for details
