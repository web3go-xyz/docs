# Ethereum Data

**chain_type**

This table shows general information about tokens on Ethereum.

| field name        | data type         | data description             |
| ------------------|:-----------------:| ---------------------------- |
| id                | integer           | Unique id                    |
| chainType         | varchar           | Chain type as token type , such as : LIT, ATA                             |
| chainName         | varchar           | Chain/token name                             |
| description       | varchar           | Description of the token                             |
| contractAddress   | varchar           | Contract address of the token                             |


**chain_type_ext**

This table shows information about the tokens in database.

| field name                  | data type         | data description             |
| ----------------------------|:-----------------:| ---------------------------- |
| id                          | integer           | unique id                    |
| contractAddress             | varchar           |                              |
| walletAddress_latest_aID    | bigint            |                              |
| lastUpdateTime              | datetime          |                              |


**wallet_address**

This table shows wallet addresses and its chain/token type on Ethereum. 

| field name                  | data type         | data description             |
| ----------------------------|:-----------------:| ---------------------------- |
| id                          | integer           | unique id                    |
| chainType                   | varchar           | Chain type as token type , such as : LIT, ATA                             |
| contractAddress             | varchar           | Contract address of the token                             |
| walletAddress               | varchar           | wallet address                             |


**wallet_address_ext**

This table shows wallet address information in database.

| field name                  | data type         | data description             |
| ----------------------------|:-----------------:| ---------------------------- |
| id                          | integer           | unique id                    |
| contractAddress             | varchar           |                              |
| walletAddress               | varchar           |                              |
| lastUpdateTime              | datetime          |                              |


**wallet_address_info**

This table shows wallet address information on Ethereum.

| field name              | data type         | data description             |
| ------------------------|:-----------------:| ---------------------------- |
| id                      | integer           | unique id                    |
| chainType               | varchar           | token type of the wallet address                             |
| contractAddress         | varchar           | contract address                             |
| walletAddress           | varchar           | wallet address                             |
| labels                  | varchar           | labels of the wallet                             |
| tokenDecimal            | integer           | token value divided by decimals                             |
| maxBalance              | decimal           | max balance of the wallet                             |
| countIn                 | integer           | Number of in-Transfer                             |
| countOut                | integer           | Number of out-Transfer                             |
| countTotal              | integer           | Number of Transfer totally                             |
| amountIn                | decimal           | In-Transfer amount                             |
| amountOut               | decimal           | Out-Transfer amount                             |
| amountTotal             | decimal           | Total Transfer amount                             |
| amountAver              | decimal           | Average amount per transfer                             |
| balance                 | decimal           | Balance of the wallet address                             |
| firstInDate             | bigint            | the timestamp (seconds) of first transaction occured for the wallet           |


**wallet_address_transaction**

This table shows the details of every transaction on Ethereum.

| field name              | data type         | data description             |
| ------------------------|:-----------------:| ---------------------------- |
| id                      | integer           | unique id                    |
| chainType               | varchar           | token type of the transaction                             |
| contractAddress         | varchar           | contract address of the transaction                             |
| walletAddress           | varchar           | wallet address                            |
| transactionTimestamp    | bigint            | transaction timestamp                             |
| direction               | integer           | transfer direction, 1=in ,2=out                             |
| amount                  | decimal           | transaction amount                             |
| balanceAtPresent        | decimal           | balance of after this transaction                             |
| hash                    | varchar           | hash of this block                            |
| from                    | varchar           | address of the transaction sender                             |
| to                      | varchar           | address of the transaction receiver                             |
