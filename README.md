# Candy Machine UI Setup Guide

This guide will walk you through the steps to set up the user interface (UI) for your Candy Machine, allowing users to mint NFTs using the SPL token you've created. The UI will use the SPL token as the payment method, and users will be able to mint NFTs by connecting their Phantom wallet.

## Prerequisites

Before you begin, make sure you have the following:

1. A Candy Machine configured with the following details in its `config.json` file:
   - `price`: 0.01
   - `number`: 10
   - `symbol`: "NB"
   - `sellerFeeBasisPoints`: 500
   - `splTokenAccount`: "GjfAchheU4qX7SJwGqPt9jXwQ32RDJhrggE3vf9wQyei"
   - `splToken`: "5BQjeXkqLFMecwAmQve8Y2XuyubPdNyQs67ANqyBsDvJ"
   - `goLiveDate`: "2022-07-24T00:00:00Z"
   - `creators`: an array with creator details

2. A Phantom wallet to act as the minting wallet.

## Steps

### 1. Set Up the SPL Token

If you haven't already, create the SPL token following the guidelines from Lesson Three. Make sure to note down the SPL token's address.

### 2. Update Candy Machine Config

Open your Candy Machine's `config.json` file and update the following fields:

- `splTokenAccount`: Update this field with the SPL token account address you've created.
- `splToken`: Update this field with the SPL token address.

### 3. Set Up the UI

Follow the steps outlined in the "Quick Node: Set Up a Minting Site" tutorial to create a user interface for your Candy Machine. This UI will allow users to connect their Phantom wallets and mint NFTs using the SPL token as payment.

### 4. Modify Minting Logic

In the minting logic of your SPL project (as per Lesson Three), make the necessary adjustments to mint NFTs to the Phantom wallet address instead of the `fromWallet`. Alternatively, adjust the transfer function to send the minted NFTs to your Phantom wallet.

### 5. Testing

Test the entire setup by transferring or minting your SPL token to one of your Phantom accounts. Then, use the UI you've created to mint NFTs. The users should be able to mint NFTs by paying in the SPL token you've set up.



## Additional Tips
- For the complete implementation of the Candy Machine logic, including minting functionality and token configuration, please refer to my [Candy Machine Repository](https://github.com/Suryajit27/Module3-Candymachine.git).
- for creating SPLtoken I referred the [The SPL token Program by MetaCrafters](https://github.com/Metacrafters/Module2-create-spl-token-js.git)
- Make sure that the addresses and token details in the `config.json` match the addresses and tokens you've created.
- Ensure that your UI provides clear instructions for users on how to connect their Phantom wallets and mint NFTs.
- You can provide further customization to your UI based on your design preferences.

## Conclusion

By following these steps, you'll have successfully set up a Candy Machine UI that allows users to mint NFTs using the SPL token you've created. Users can connect their Phantom wallets and use the SPL token as payment to mint NFTs from your Candy Machine. Remember to thoroughly test the setup before deploying it for public use.
