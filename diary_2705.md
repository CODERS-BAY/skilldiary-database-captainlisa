# Diary 27.05.2020

## Transactions

    ```sql
    begin transaction;
        update ...;
        update ...;
    commit;
    ```

* actions that change the structure of a database (like CREATE TABLE, ALTER TABLE) are always transactions
* 2-Phase-Commit-Protocol are transactions that tell two computers to communicate. NO1 requests if NO2 is ready for a transaction, NO2 says yes, NO1 sends commit and NO2 reports back if commit was successful.
* flat transactions when one start server sends information to many endservers. 
* nested transactions = when one start server sends information to other servers and those distributes the information to the endclients.
* the word ```commit``` ends one transaction and automatically starts a new one.
* autonomous transactions are independent from other transactions in the process. an example for that are so-called demon transactions that happen at night, for example every night the server deletes all entries that are older than 2 years.
* as a rule we hold transactions open as long as needed but as short as possible.
* it's also important to only lock one data entry at a time
* locking a data entry avoids Phantom Read Problems. Example: if one person reservers a seat on a plane and does not lock the entry, the seat is theoretically taken, but another person still has access to that entry and can see it. 
* a chain of transactions makes a rollback impossible, since the different parts of the chain are committed one after the other. the only way to reverse that would be compensation, which means to set back all the values in the entries by hand. 
* savepoints are a way to rollback to previous points of the transaction.
* there are four main commands for transaction control:
  * ```commit```
  * ```rollback```
  * ```savepoint```
  * ```set transaction```
* with ```set transaction``` you can set a transaction to "read only" for example, and also set it to write.
* 