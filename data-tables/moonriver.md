# Moonriver

**collator_action_history**

This table shows the history of collators' action events and the corresponding balance change.

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           | unique id                    |
| roundindex        | integer           | round index                     |
| account           | varchar           | collator account                     |
| actiontype        | varchar           | action type name                     |
| balancechange     | decimal           | balance change in the action                     |
| balancecurrent    | decimal           | balance current in the action                     |
| blocknumber       | bigint            | the block number where the action took place                      |
| timestamp         | varchar           | timestamp when the action took place                     |


**collator_number_history**

This table shows the history of changes of the number of collators.

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           | unique id                     |
| blocknumber       | bigint            | the block number where the change took place    |
| roundindex        | integer           | round index                     |
| old               | integer           | old number of collators                    |
| new               | integer           | new number of collators                    |
| timestamp         | varchar           | the timestamp when the change took place                      |

**collator_point_history**

This table shows the history of collators getting points after generating a block.

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           | unique id                     |
| roundindex        | integer           | round index                     |
| account           | varchar           | collator account                     |
| point             | integer           | the point that the collator has got                     |
| blocknumber       | bigint            | the block number where the collator got the point                     |

**nominator_action_history**

This table shows the history of nominators nominating a collator and the corresponding balance change.

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           | unique id                     |
| roundindex        | integer           | round index                     |
| account           | varchar           | nominator account                     |
| collator          | varchar           | collator account                     |
| actiontype        | varchar           | action type of the nomination                     |
| balancechange     | decimal           | balance change in the nomination                     |
| balancecurrent    | decimal           | balance current in the nomination                     |
| blocknumber       | bigint            | the block number where the nomination took place                     |
| timestamp         | varchar           | the timestamp when the nomination took place                     |

**reward_history**

This table shows the history of collators and nominators getting rewards for the finished block generations.

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           | unique id                     |
| account           | varchar           | the collator/nominator account                     |
| issueBlock        | bigint            | the block where the reward was issued                     |
| issueroundindex   | bigint            | the round index when the reward was issued                     |
| realroundindex    | bigint            | real round index                     |
| balance           | decimal           | balance of the account                     |
| timestamp         | varchar           | the timestamp when the reward was issued                     |
| isCollator        | integer           | if the reward getter is a collator                     |
| isNominator       | integer           | if the reward getter is a nominator                    |

**round_collator**

This table shows the bond information of collators at the start of each round.

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           | unique id                     |
| roundindex        | integer           | round index                     |
| account           | varchar           | collator account                    |
| selfbond          | decimal           |                      |
| totalbond         | decimal           |                      |

**round_info**

This table shows the general information of each round such as number of collators involved, total bond and start block.

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           | unique id                     |
| roundindex        | integer           | round index                     |
| numberOfCollator  | integer           | number of collators in the round                     |
| totalbond         | decimal           | total bond of the round                     |
| startblock        | bigint            | start block of the round                     |
| timestamp         | varchar           | the timestamp when round got started                     |
