# Zardkat: Zero-Knowledge Proof Generator 

Zardkat is a cutting-edge template based on [hardhat-circom](https://github.com/projectsophon/hardhat-circom) that empowers developers to create and deploy zero-knowledge proof circuits, proofs, and corresponding Solidity verifiers.

## Getting Started
Clone this repository to your local machine.

```bash
git clone https://github.com/syedwaheedulla/ZK-SNARK-Designer.git
cd K-SNARK-Designe
```

Follow these steps to compile the Multiplier2() circuit and verify it through a smart contract verifier.

```circom
pragma circom 2.0.0;

// Define a circuit that checks whether 'c' is the result of 'a' multiplied by 'b'.
template Multiplier2 () {  
   signal input a;  
   signal input b;  
   signal output c;  
   c <== a * b;  
}
component main = Multiplier2();

#Installation
Run the following command to install the required dependencies:
```bash
npm install
'''

#Compilation
Execute the command below to compile the circuit:
```bash
npx hardhat circom
'''

This will generate the out folder containing circuit intermediaries, as well as the MultiplierVerifier.sol contract.

#Proving and Deploying
Run the script to deploy the MultiplierVerifier contract, generate a proof from circuit intermediaries, generate calldata, and finally, verify the proof:
```bash
npx hardhat run scripts/deploy.ts
'''

#This script performs the following actions:

1.Deploys the MultiplierVerifier.sol contract.
2.Generates a proof using generateProof().
3.Creates calldata using generateCallData().
4.Calls the verifyProof() function on the verifier contract with the calldata.
5.In just two commands, you can compile a Zero-Knowledge Proof, generate a proof, deploy a verifier, and validate the proof.
Celebrate your success! 🎉


