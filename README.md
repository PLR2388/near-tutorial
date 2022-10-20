# near-tutorial

## near-cli

To login: `near login` 

To create a subaccount: `near create-account ${SUBACCOUNT_ID}.${ACCOUNT_ID} --masterAccount ${ACCOUNT_ID} --initialBalance ${INITIAL_BALANCE}` 

To compile the contract: `yarn asb`

To deploy the contract: `near deploy --accountId=${ACCOUNT_ID} --wasmFile=${PATH_TO_WASM}`

To call a view or change function via cli : `near call ${CONTRACT_ACCOUNT_ID} ${METHOD_NAME} ${PAYLOAD} --accountId=${ACCOUNT_ID}`
For instance, it looks like this with the project : `near call mycontract.myaccount.testnet setProduct '{"id": "0", "productName": "tea"}' --accountId=myaccount.testnet`