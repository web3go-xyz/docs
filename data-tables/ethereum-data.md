# Ethereum Data

**chain_type**

This table shows general information about parachains on Kusama.

| field name        | data type         | data description             |
| ------------------|:-----------------:| ---------------------------- |
| id                | integer           | unique id                    |
| chainType         | varchar           |                              |
| chainName         | varchar           |                              |
| description       | varchar           |                              |
| contractAddress   | varchar           |                              |


**chain_type_ext**

This table shows general information about parachains on Kusama.

| field name                  | data type         | data description             |
| ----------------------------|:-----------------:| ---------------------------- |
| id                          | integer           | unique id                    |
| contractAddress             | varchar           |                              |
| walletAddress_latest_aID    | bigint            |                              |
| lastUpdateTime              | datetime          |                              |


**wallet_address**

This table shows general information about parachains on Kusama.

| field name                  | data type         | data description             |
| ----------------------------|:-----------------:| ---------------------------- |
| id                          | integer           | unique id                    |
| chainType                   | varchar           |                              |
| contractAddress             | varchar           |                              |
| walletAddress               | varchar           |                              |


**wallet_address_ext**

This table shows general information about parachains on Kusama.

| field name                  | data type         | data description             |
| ----------------------------|:-----------------:| ---------------------------- |
| id                          | integer           | unique id                    |
| contractAddress             | varchar           |                              |
| walletAddress               | varchar           |                              |
| lastUpdateTime              | datetime          |                              |


**wallet_address_info**

This table shows general information about parachains on Kusama.

| field name              | data type         | data description             |
| ------------------------|:-----------------:| ---------------------------- |
| id                      | integer           | unique id                    |
| chainType               | varchar           |                              |
| contractAddress         | varchar           |                              |
| walletAddress           | varchar           |                              |
| labels                  | varchar           |                              |
| tokenDecimal            | integer           |                              |
| maxBalance              | decimal           |                              |
| countIn                 | integer           |                              |
| countOut                | integer           |                              |
| countTotal              | integer           |                              |
| amountIn                | decimal           |                              |
| amountOut               | decimal           |                              |
| amountTotal             | decimal           |                              |
| amountAver              | decimal           |                              |
| balance                 | decimal           |                              |
| firstInDate             | bigint            |                              |


**wallet_address_transaction**

This table shows general information about parachains on Kusama.

| field name              | data type         | data description             |
| ------------------------|:-----------------:| ---------------------------- |
| id                      | integer           | unique id                    |
| chainType               | varchar           |                              |
| contractAddress         | varchar           |                              |
| walletAddress           | varchar           |                              |
| transactionTimestamp    | bigint            |                              |
| direction               | integer           |                              |
| amount                  | decimal           |                              |
| balanceAtPresent        | decimal           |                              |
| hash                    | varchar           |                              |
| from                    | varchar           |                              |
| to                      | varchar           |                              |
