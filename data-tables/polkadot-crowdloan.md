# Polkadot Crowdloan

**polk_para_chain**

This table shows general information about parachains on Polkadot.

| field name        | data type         | data description             |
| ------------------|:-----------------:| ---------------------------- |
| id                | integer           | Unique id                    |
| paraId            | varchar           | Parachain ID                             |
| projectName       | varchar           | Project name                             |
| icon              | varchar           | Icon for parachain                             |
| lastUpdateTime    | datetime          | Last update time of paraChain                             |


**polk_para_chain_crowdloan**

This table shows all the crowdloan information on Polkadot.

| field name        | data type         | data description             |
| ------------------|:-----------------:| ---------------------------- |
| id                | integer           | Unique id                    |
| paraId            | varchar           | Parachain ID                             |
| crowdloanId       | varchar           | Crowdloan ID, alias funds.edges.node.id                             |
| firstLease        | integer           | Alias firstSlot, of the crowdloan                             |
| lastLease         | integer           | Alias lastSlot, of the crowdloan                             |
| raised            | bigint            | Raised amount of the crowdloan                             |
| cap               | bigint            | Total capital requirement for the crowdloan                             |
| expirationBlock   | integer           | Expiration block of the crowdloan, indicating a specific round in KSM crowdloan        |
| status            | varchar           | Status of the crowdloan                             |


**polk_para_chain_crowdloan_contribution**

This table shows all the crowdloan contribution information on Polkadot

| field name        | data type         | data description             |
| ------------------|:-----------------:| ---------------------------- |
| id                | integer           | Unique id                    |
| crowdloanId       | varchar           | Crowdloan ID, alias funds.edges.node.id                             |
| contributionId    | varchar           | Contribution ID, alias contributions.edges.node.id                             |
| account           | varchar           | Account that made the contribution                             |
| amount            | double            | Amount of the contribution                             |
| blockNum          | integer           | The block number where the contribution took place                             |
| createAt          | datetime          | The date and time when the contribution was created                             |

**polk_para_chain_crowdloan_contribution_proxy_detail**

This table shows all the crowdloan contribution information on Polkadot

| field name        | data type         | data description             |
| ------------------|:-----------------:| ---------------------------- |
| id                | integer           | Unique id                    |
| crowdloanId       | varchar           | Crowdloan ID, alias funds.edges.node.id                             |
| contributionAccount           | varchar           | Account that made the contribution                             |
| amount            | double            | Amount of the contribution                             |
| blockHeightOnProxy          | integer           | The block number where the contribution took place on Polkadot                            |
| createAtOnProxy          | datetime          | The date and time when the contribution was created on Polkadot                            |
