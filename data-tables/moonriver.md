# Moonriver

**collator_action_history**

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           |                      |
| roundindex        | integer           |                      |
| account           | varchar           |                      |
| actiontype        | varchar           |                      |
| balancechange     | decimal           |                      |
| balancecurrent    | decimal           |                      |
| blocknumber       | bigint            |                      |
| timestamp         | varchar           |                      |


**collator_number_history**

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           |                      |
| blocknumber       | bigint            |                      |
| roundindex        | integer           |                      |
| old               | integer           |                      |
| new               | integer           |                      |
| timestamp         | varchar           |                      |

**collator_point_history**

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           |                      |
| roundindex        | integer           |                      |
| account           | varchar           |                      |
| point             | integer           |                      |
| blocknumber       | bigint            |                      |

**moon_river_chain_state**

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           |                      |
| chain             | varchar           |                      |
| wssEndpoint       | varchar           |                      |
| symbol            | varchar           |                      |
| startRoundIndex   | bigint            |                      |
| startTimestamp    | varchar           |                      |
| maxCollatorCount  | integer           |                      |
| maxNominatorCount | integer           |                      |

**nominator_action_history**

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           |                      |
| roundindex        | integer           |                      |
| account           | varchar           |                      |
| collator          | varchar           |                      |
| actiontype        | varchar           |                      |
| balancechange     | decimal           |                      |
| balancecurrent    | decimal           |                      |
| blocknumber       | bigint            |                      |
| timestamp         | varchar           |                      |

**reward_history**

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           |                      |
| account           | varchar           |                      |
| issueBlock        | bigint            |                      |
| issueroundindex   | bigint            |                      |
| realroundindex    | bigint            |                      |
| balance           | decimal           |                      |
| timestamp         | varchar           |                      |
| isCollator        | integer           |                      |
| isNominator       | integer           |                      |

**round_collator**

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           |                      |
| roundindex        | integer           |                      |
| account           | varchar           |                      |
| selfbond          | decimal           |                      |
| totalbond         | decimal           |                      |

**round_info**

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           |                      |
| roundindex        | integer           |                      |
| numberOfCollator  | integer           |                      |
| totalbond         | decimal           |                      |
| startblock        | bigint            |                      |
| timestamp         | varchar           |                      |
