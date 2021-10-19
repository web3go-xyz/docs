# KSM Crowdloan

**polk_para_chain**

This table shows general information about parachains on Kusama.

| field name        | data type         | data description             |
| ------------------|:-----------------:| ---------------------------- |
| id                | integer           | unique id                    |
| paraId            | varchar           |                              |
| projectName       | varchar           |                              |
| icon              | varchar           |                              |
| lastUpdateTime    | datetime          |                              |


**polk_para_chain_crowdloan**

This table shows all the crowdloan information on Kusama.

| field name        | data type         | data description             |
| ------------------|:-----------------:| ---------------------------- |
| id                | integer           | unique id                    |
| paraId            | varchar           |                              |
| crowdloanId       | varchar           |                              |
| firstLease        | integer           |                              |
| lastLease         | integer           |                              |
| raised            | bigint            |                              |
| cap               | bigint            |                              |
| expirationBlock   | integer           |                              |
| status            | varchar           |                              |


**polk_para_chain_crowdloan_contribution**

This table shows all the crowdloan contribution information on Kusama

| field name        | data type         | data description             |
| ------------------|:-----------------:| ---------------------------- |
| id                | integer           | unique id                    |
| crowdloanId       | varchar           |                              |
| contributionId    | varchar           |                              |
| account           | varchar           |                              |
| amount            | double            |                              |
| blockNum          | integer           |                              |
| createAt          | datetime          |                              |


