# Diary 18.03.2020

## Database
* for complex interactions--like transferring money between bank accounts, it is important to make sure change that is happening does not cause any anomalies
* in that case it is best to use a transaction.
* A transaction is a set of operations that must all be completed, and if for some reason any of the individual operations aren't completed, no changes are made to the database.
* Transactions follow a set of principles, which it has tu fullfill: ACID
  * Atomic
  * Consistent
  * Isolated
  * Durable
* Anytime we have an activity made up of steps that must happen together, and we want to ensure that we have exclusive access to certain information while we perform a task, we'll use a transaction.