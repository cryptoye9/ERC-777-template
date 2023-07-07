# ERC-777 Token Standard

## Concept

**ERC-777** is an extension of the ERC-20 token standard on the Ethereum blockchain. It aims to **enhance the functionality and capabilities** of tokens by introducing new features while **maintaining backward compatibility** with ERC-20 tokens.

## Main Features and Difference from ERC-20

1. **Backward Compatibility**: ERC-777 tokens are designed to be fully **backward compatible** with ERC-20 tokens.

2. **Operator Mechanism**: ERC-777 introduces the concept of an **"operator"**. Token holders can authorize specific addresses as operators, allowing them to send tokens on behalf of the token holders.

3. **Hooks**: ERC-777 introduces **hooks**, which are callback functions that can be triggered during token transfers.

4. **Granular Control over Transfers**: ERC-777 allows token contracts to define their own **transfer logic**.

5. **Improved User Experience**: ERC-777 aims to enhance the user experience by providing more **informative and descriptive error messages** during token transfers.

## Problems with the ERC-777 Standard

1. **Hooks attack vector**: This bug takes advantage of the ERC777 feature that enables setting a hook receiver. By exploiting the ability to make arbitrary calls in a target contract, a malicious caller can call the ERC777 registry contract and assign a specific hook address to the target contract. As a result, whenever the target contract receives ERC777 tokens in the future, the attacker’s hook smart contract will be triggered.

2. **Complexity**: The additional features introduced by ERC-777 may increase the **complexity** of token contracts.

## How to Use ERC-777

To use the ERC-777 standard, follow these steps:

1. Implement the ERC-777 token contract by extending the standard ERC-777 contract OR you might take it from this repository.
2. Define any additional functionalities specific to your token, such as custom transfer restrictions, hooks, or operator permissions.
3. Test the token contract thoroughly to ensure it functions as intended and adheres to security best practices.
4. Deploy the token contract on the Ethereum blockchain.
5. Communicate the deployment of your ERC-777 token to users, exchanges, and dApps to enable integration and adoption.

It's important to note that the actual usage and implementation details of ERC-777 may vary based on specific requirements and use cases. It is recommended to refer to the official ERC-777 documentation, community resources, and best practices for a more comprehensive understanding of the standard and its implementation.
