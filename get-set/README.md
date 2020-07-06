# Xooa Get-Set Smart Contract

This page provides an overview to Xooa Get-Set Smart Contract functionalities.

This smart contract runs on `Hyperledger Fabric` and is written in `GoLang`.

Originally created by IBM and forked from [here](https://hyperledger-fabric.readthedocs.io/en/release-1.2/chaincode4ade.html#pulling-it-all-together).

## Overview

This smart contract provides 3 functions:
  
  * Get
  * Set
  * GetVersion


#### Get

Get method is used to fetch the value associated with a key passed in the arguments.
This method expects a single argument as the key whose world state is required.
If a value is found for the key then it returns the value or else it returns an error message.


#### Set

Set method is used to store the key value pair in the ledger.
This method requires two arguments and takes the first as the key and second as value.
This method creates a transaction in the blockchain ledger and stores the key value pair.
If it succeeds in creating the transaction it returns a response with key value pair as payload or else an error response.


#### GetVersion

This method is used to get the version of the chaincode that is deployed.
It returns the chaincode name and the version number for it.



## Deploy the Get-Set smart contract 
 
1. Follow the instructions here: https://docs.xooa.com/start.html#deploy-the-smart-contract-app, selecting the **Xooa-Get-Set** as the smart contract.

2. Record the **API Token** when it is shown: you will need it to authorize API requests from Dropbox App.

   > **Tip:**  to regenerate the API token: 
   >
   > 1. Go to the **Identities** tab in the App. 
   > 2. Next to the ID, select **Actions**.
   > 3. Select **Regenerate API Token**, and then select **Generate**.



## Explore the get-set smart Contract end-points

1. Go to the **API** tab, and then click **Explore APIs**.

2. Enter **API Token** in the field in navigation pane.

3. Go to **Smart Contract > Invoke Smart Contract Function**.

  	**Invoke** will write to the blockchain. The function **set** is used to invoke the smart contract.

  	**Query** will read data from the blockchain. The function **get** is used to query the smart contract.

4. In the **fcn** field, enter `set`.

5. In the **body** field, enter the data you want to store in the blockchain in the format:

  	`[ "<key>", "<value>" ]`

6. Click **try**. 

> **Congrats!** You have saved data in a blockchain using **Xooa**.

7. To view your transaction as part of the blockchain, go to [https://xooa.com/blockchain](https://xooa.com/blockchain/ledger?utm_source=samplesRepo) or navigate to **Ledger** from your Xooa console.

8. Navigate to **Transactions** tab.

9. You can expand the data field to see your transactions.


## What is swagger.json and it's purpose

Swagger is used to simplify API development and is used by Xooa for defining REST APIs. 
Using swagger Xooa provides you an interface to make API requests.
Place **swagger.json** file along with your Smart Contract and Xooa will pick it up while deploying and will integrate it with your app.

### Steps to access [swagger](https://docs.xooa.com/API.html)

1. Go to [https://xooa.com/blockchain](https://xooa.com/blockchain/custom-smart-contracts?utm_source=samplesRepo) or navigate to **Custom Smart Contracts** from your Xooa console.

2. Click **Deploy New** or select an existing app to upgrade.

3. Once the app is deployed or upgraded successfully, Navigate to **API** tab and select **Sandbox** option and there you will find API Explorer.

4. Paste API token in the required input box and click on **Authorize API** to access swagger REST APIs.