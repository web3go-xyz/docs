# Karura

**chain_state**

This table shows the state of the Karura chain such as websocket endpoint, stability fee percentage.

| field name                     | data type         | data description             |
| -------------------------------|:-----------------:| ---------------------------- |
| id                             | integer           | Unique id                    |
| chain                          | varchar           | chain name                             |
| wssEndpoint                    | varchar           | websocket endpoint                             |
| symbol                         | varchar           | the symbol name like : KSM                             |
| latestUpdateTimestamp          | bigint            | latest update timestamp                             |
| stabilityFeePercentage         | decimal           | The percentage of required stability fee                             |
| liquidationRatioPercentage     | decimal           | The percentage of liquidation ratio                             |
| liquidationPenaltyPercentage   | decimal           | The percentage of liquidation for penalty                             |
| requiredCollateralRatioPercentage | decimal        | The percentage of required collateral ratio                             |


**chain_statistic** 

This table shows statistics of the chain such as debit and collateral data.

| field name                  | data type         | data description             |
| ----------------------------|:-----------------:| ---------------------------- |
| id                          | integer           | Unique id                    |
| chain                       | varchar           | the chain name                             |
| tokenId                     | varchar           | the token name like : KSM                             |
| totalCount                  | bigint            | total count of loanPosition                             |
| debit                       | decimal           | total debit                             |
| collateral                  | decimal           | total collateral                             |
| latestUpdateTimestamp       | bigint            | the latest update timestamp                             |
| debitFormat                 | decimal           | total debit formated with scale                             |
| collateralFormat            | decimal           | total collateral formated with scale                             |
| collateralPrice             | decimal           | price of  collateral at this very moment                             |


**loan_action**

This table shows records of loan actions and corresponding data on Karura.

| field name                  | data type         | data description             |
| ----------------------------|:-----------------:| ---------------------------- |
| id                          | integer           | unique id                    |
| chain                       | varchar           | the chain name                             |
| tokenId                     | varchar           | the token name like : KSM                             |
| accountId                   | varchar           | accountId of current loanAction                             |
| actionId                    | varchar           | actionId of current loanAction                             |
| type                        | varchar           | type of current loanAction                             |
| subType                     | varchar           | sub-type of current loanAction                             |
| timestamp                   | bigint            | timestamp when action occured                             |
| data_original               | text              | original data as JSON                             |
| debitAdjustment             | decimal           | debit adjustment of this loanAction                             |
| debit                       | decimal           | debit after this loanAction                             |
| collateralAdjustment        | decimal           | collateral adjustment of this LoanAction                             |
| collateral                  | decimal           | collateral after this LoanAction                             |
| debitFormat                 | decimal           | debit formated with scale                             |
| collateralFormat            | decimal           | collateral formated with scale                             |
| collateralPrice             | decimal           | price of collateral at this very moment                             |
| ratioPercentage             | decimal           | ratio percentage calculated at this very moment                             |
| status                      | varchar           | status of current loanAction: Safe, Warning, Danger                             |
| debitAdjustment_balance     | decimal           | debit adjustment of this loanAction when  ConfiscateCollateralAndDebit triggered  |
| collateralAdjustment_balance| decimal           | collateral adjustment of this LoanAction when ConfiscateCollateralAndDebit triggered |
| blockNumber                 | bigint            | blockNumber of current loanAction                             |
| blockId                     | varchar           | blockId of current loanAction                             |
| extrinsicId                 | varchar           | extrinsicId of current loanAction                             |


**loan_position**

This table shows records of loan actions and corresponding data on Karura

| field name              | data type         | data description             |
| ------------------------|:-----------------:| ---------------------------- |
| id                      | integer           | Unique id                    |
| chain                   | varchar           | the chain name                             |
| tokenId                 | varchar           | the token name like : KSM                             |
| accountId               | varchar           | accountId of current loanPosition                             |
| debit                   | decimal           | debit of current loanPosition                             |
| collateral              | decimal           | collateral of current loanPosition                             |
| latestUpdateTimestamp   | bigint            | the latest update timestamp                            |
| ratioPercentage         | decimal           | ratio percentage calculated at this very moment                             |
| status                  | varchar           | status of current loanPosition: Safe, Warning, Danger                             |
| debitFormat             | decimal           | debit formated with scale                             |
| collateralFormat        | decimal           | collateral formated with scale                             |
| collateralPrice         | decimal           | price of collateral at this very moment                             |


**price**

This table shows the statistic of price during the time period.

| field name              | data type         | data description             |
| ------------------------|:-----------------:| ---------------------------- |
| id                      | integer           | Unique id                    |
| symbol                  | varchar           | the symbol name like : KSMUSDT, KSMBUSD                             |
| timeIndicator           | bigint            | the time indicator, should be matched with minutes scale                             |
| openTime                | bigint            | Open time for current price                             |
| closeTime               | bigint            | Close time for current price                             |
| openPrice               | decimal           | Open price during the period                            |
| highPrice               | decimal           | High price during the period                            |
| lowPrice                | decimal           | Low price during the period                            |
| closePrice              | decimal           | Close price during the period                            |


**price_fetch_task**

This table shows the tasks for fetching prices.

| field name            | data type         | data description             |
| ----------------------|:-----------------:| ---------------------------- |
| id                    | integer           | Unique id                    |
| symbol                | varchar           | the symbol name like : KSMUSDT, KSMBUSD                             |
| latestPriceTimestamp  | bigint            | the latest price timestamp                             |
| api_url               | varchar           | the api url for Binance                             |
| apiKey                | varchar           | the apiKey                             |
| apiSecret             | varchar           | the apiSecret                             |
| interval              | varchar           | the price kline interval, such as : 1m                             |
| limit                 | integer           | the price count in the fetch range                             |
| timeStep              | bigint            | the time step in milliseconds, default is 1hour= 60 * 60 * 1000     |










