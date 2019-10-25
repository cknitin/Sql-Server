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


#### Phantom read 

   
