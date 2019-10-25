# Isolation Level in Sql Server

## Types of Isolation level

#### 1. Read Uncommited
#### 2. Read commited
#### 3. Repeatable read
#### 4. Snapshot
#### 5. Serializable 


### Example

    SET TRANSACTION ISOLATION LEVEL
    { READ UNCOMMITTED
    | READ COMMITTED
    | REPEATABLE READ
    | SNAPSHOT
    | SERIALIZABLE
    }
    
    
## Isolation level 

#### Dirty Read
Transaction T1 modified some data, after the modification transaction T2 read this modified data before the comit of transaction T1.

#### Nonrepeatable read
Transaction T1 get a row of data from a table. T2 updates that row. T1 tries to get this row again in the same transaction, but get diffrent result because of the T2 modified that data.


#### Phantom read 
T1 get some rows of data from a table. T2 inserts a new row into the same table, Now T1 perform same query with same condition but get extra row , this extra row called phantom row.



| Isolation Level     | Dirty Read | Nonrepeatable read | Phantom read |
|---------------------|------------|--------------------|--------------|
| READ UNCOMMITTED    |   Yes      |      Yes           |     Yes      |    
| READ COMMITTED      |   No       |      Yes           |     Yes      |    
| REPEATABLE READ     |   No       |      No            |     Yes      |
| SERIALIZABLE        |   No       |      No            |     No       |          
| SNAPSHOT            |   No       |      No            |     No       |






   
