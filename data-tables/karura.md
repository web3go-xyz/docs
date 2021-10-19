# Karura

**chain_state**

This table shows

| field name                     | data type         | data description             |
| -------------------------------|:-----------------:| ---------------------------- |
| id                             | integer           | unique id                    |
| chain                          | varchar           |                              |
| wssEndpoint                    | varchar           |                              |
| symbol                         | varchar           |                              |
| latestUpdateTimestamp          | bigint            |                              |
| stabilityFeePercentage         | decimal           |                              |
| liquidationRatioPercentage     | decimal           |                              |
| liquidationPenaltyPercentage   | decimal           |                              |
| requiredCollateralRatioPercentage | decimal        |                              |


**chain_statistic**

This table shows

| field name                  | data type         | data description             |
| ----------------------------|:-----------------:| ---------------------------- |
| id                          | integer           | unique id                    |
| chain                       | varchar           |                              |
| tokenId                     | varchar           |                              |
| totalCount                  | bigint            |                              |
| debit                       | decimal           |                              |
| collateral                  | decimal           |                              |
| latestUpdateTimestamp       | bigint            |                              |
| debitFormat                 | decimal           |                              |
| collateralFormat            | decimal           |                              |
| collateralPrice             | decimal           |                              |


**loan_action**

This table shows 

| field name                  | data type         | data description             |
| ----------------------------|:-----------------:| ---------------------------- |
| id                          | integer           | unique id                    |
| chain                       | varchar           |                              |
| tokenId                     | varchar           |                              |
| accountId                   | varchar           |                              |
| actionId                    | varchar           |                              |
| type                        | varchar           |                              |
| subType                     | varchar           |                              |
| timestamp                   | bigint            |                              |
| data_original               | text              |                              |
| debitAdjustment             | decimal           |                              |
| debit                       | decimal           |                              |
| collateralAdjustment        | decimal           |                              |
| collateral                  | decimal           |                              |
| debitFormat                 | decimal           |                              |
| collateralFormat            | decimal           |                              |
| collateralPrice             | decimal           |                              |
| ratioPercentage             | decimal           |                              |
| status                      | varchar           |                              |
| debitAdjustment_balance     | decimal           |                              |
| collateralAdjustment_balance| decimal           |                              |
| blockNumber                 | bigint            |                              |
| blockId                     | varchar           |                              |
| extrinsicId                 | varchar           |                              |


**loan_position**

This table shows 

| field name              | data type         | data description             |
| ------------------------|:-----------------:| ---------------------------- |
| id                      | integer           | unique id                    |
| chain                   | varchar           |                              |
| tokenId                 | varchar           |                              |
| accountId               | varchar           |                              |
| debit                   | decimal           |                              |
| collateral              | decimal           |                              |
| latestUpdateTimestamp   | bigint            |                              |
| ratioPercentage         | decimal           |                              |
| status                  | varchar           |                              |
| debitFormat             | decimal           |                              |
| collateralFormat        | decimal           |                              |
| collateralPrice         | decimal           |                              |


**price**

This table shows

| field name              | data type         | data description             |
| ------------------------|:-----------------:| ---------------------------- |
| id                      | integer           | unique id                    |
| symbol                  | varchar           |                              |
| timeIndicator           | bigint            |                              |
| openTime                | bigint            |                              |
| closeTime               | bigint            |                              |
| openPrice               | decimal           |                              |
| highPrice               | decimal           |                              |
| lowPrice                | decimal           |                              |
| closePrice              | decimal           |                              |


**price_fetch_task**

This table shows

| field name            | data type         | data description             |
| ----------------------|:-----------------:| ---------------------------- |
| id                    | integer           | unique id                    |
| symbol                | varchar           |                              |
| latestPriceTimestamp  | bigint            |                              |
| api_url               | varchar           |                              |
| apiKey                | varchar           |                              |
| apiSecret             | varchar           |                              |
| interval              | varchar           |                              |
| limit                 | integer           |                              |
| timeStep              | bigint            |                              |










