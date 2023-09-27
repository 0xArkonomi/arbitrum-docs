## Add Testnet Orbit Chain to the Arbitrum Bridge 

Prerequisites 
- Orbit Local Devnet Chain (to create a Orbit Local Devnet Chain follow the steps in https://docs.arbitrum.io/launch-orbit-chain/orbit-quickstart) 

1. Navigate to https://bridge.arbitrum.io/
2. Connect to Arbitrum Goerli or Sepolia and the bridge page will automatically switch to the correct testnet view
3. If you are connected to mainnet, and don’t switch networks manually in your wallet, then you can enable testnet mode in the bridge by clicking on your address in the top right --> clicking "settings" --> and then "turn on testnet mode".
4. Go to settings and scroll down to “Add testnet Orbit chain”
   ![orbit chain panel](../assets/orbit-chain-panel.png)
5. Insert the JSON configuration from the `outputInfo.json` file that's generated into the Orbit Testnet Bridge.
6. Click “Add chain” Button
7. Then your chain will appear in both the network drop down in the top navigation, and as an option in the bridging interface directly.