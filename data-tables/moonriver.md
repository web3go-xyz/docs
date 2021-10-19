# Moonriver

**collator_action_history**

This table shows the history of action events and the corresponding balance change.

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

This table shows the history of changes of the number of collators.

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           |                      |
| blocknumber       | bigint            |                      |
| roundindex        | integer           |                      |
| old               | integer           |                      |
| new               | integer           |                      |
| timestamp         | varchar           |                      |

**collator_point_history**

This table shows the history of collators getting points after generating a block.

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           |                      |
| roundindex        | integer           |                      |
| account           | varchar           |                      |
| point             | integer           |                      |
| blocknumber       | bigint            |                      |

**nominator_action_history**

This table shows the history of nominators nominating a collator and the corresponding balance change.

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

This table shows the history of collators and nominators getting rewards for the finished block generations.

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

This table shows the bond information of collators at the start of the each round.

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           |                      |
| roundindex        | integer           |                      |
| account           | varchar           |                      |
| selfbond          | decimal           |                      |
| totalbond         | decimal           |                      |

**round_info**

This table shows the general information of each round such as number of collators involved, total bond and start block.

| field name        | data type         | data description     |
| ------------------|:-----------------:| --------------------:|
| id                | integer           |                      |
| roundindex        | integer           |                      |
| numberOfCollator  | integer           |                      |
| totalbond         | decimal           |                      |
| startblock        | bigint            |                      |
| timestamp         | varchar           |                      |
