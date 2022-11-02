# near-tutorial

## near-cli

To login: `near login` 

To create a subaccount: `near create-account ${SUBACCOUNT_ID}.${ACCOUNT_ID} --masterAccount ${ACCOUNT_ID} --initialBalance ${INITIAL_BALANCE}` 

To compile the contract: `yarn asb`

To deploy the contract: `near deploy --accountId=${ACCOUNT_ID} --wasmFile=${PATH_TO_WASM}`

To call a change function via cli : `near call ${CONTRACT_ACCOUNT_ID} ${METHOD_NAME} ${PAYLOAD} --accountId=${ACCOUNT_ID}`
For instance, it looks like this with the project : `near call mycontract.myaccount.testnet setProduct '{"id": "0", "productName": "tea"}' --accountId=myaccount.testnet`
Calling a change function cost gas.

To call a view function via cli : `near view ${CONTRACT_ACCOUNT_ID} ${METHOD_NAME} ${PAYLOAD}`. It doesn't cost gas to view.

## Contract

To compile the contract : `yarn asb`

To do a token transfer: `ContractPromiseBatch.create(${RECEIVING_ACCOUNT}).transfer(${DEPOSIT});`

## Rust

To compile the project : `RUSTFLAGS='-C link-arg=-s' cargo build --target wasm32-unknown-unknown --release`

To recompile a project with Rust, there are 2 solutions: delete the account linked to the contract or used dev_deploy

`near delete mycontract.myaccount.testnet myaccount.testnet `