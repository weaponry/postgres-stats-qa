# PostgreSQL activity statistics: Questions and Answers. 

This is a list of questions which might occur during PostgreSQL administration and possible ways of how to answer on these questions.

This should be used with [pgstats.dev](https://pgstats.dev)

## Content

1. [Client Backends](https://pgstats.dev/Client%20Backends)
    - what is client backend?
    - how many clients connected to the server?
    - how many clients connected to the database?
    - how many clients connected remotely?
    - what states of connected clients?
    - are there any blocked clients?
    - do the connected clients use SSL?
    - is there any long queries or transactions on the server?
    - how much time spent by sessions?
    - how many sessions were established and terminated?
    

2. [Query Planning](https://pgstats.dev/Query%20Planning)
    - what is planner?
    - how long queries are planned?
    - what is the ratio of planning time to executing time?
    - how to get plan of the query?


3. [Query Execution](https://pgstats.dev/Query%20Execution)
    - what is query executor?
    - how many queries executed on the server, database, or from specific address?
    - what queries are executed right now?
    - is there any blocked/waiting transactions or queries?
    - what the top of wait events occurs right now?
    - what is the duration of the running xacts and queries?
    - how much time my functions are executed?
    - how much time my queries are executed?
    - how many times my queries have been called?
    - how much time my queries are executed?
    - how much time my queries spent doing IO?
    - how many locks and what types of locks on the server?
    - how much time waiting queries are waiting?
    - how many of specific queries are executed now? how many SELECTS, UPDATES, and so on.
    - how many CREATE INDEX opearions are running and what its progress?
    - how many CLUSTER or VACUUM FULL opearions are running and what its progress?
    - how many COPY opearions are running and what its progress?


4. [Tables Usage](https://pgstats.dev/Tables%20Usage)
    - what is tables?
    - how many tables in my database?
    - how my tables are accessed and how many rows retrieved?
    - what workload is on my tables?


5. [Indexes Usage](https://pgstats.dev/Indexes%20Usage)
    - what is the main purpose of indexes?
    - how many indexes is in my database or table?
    - how often my indexes are used?


6. [Buffers IO](https://pgstats.dev/Buffers%20IO)
    - what is buffers IO?
    - how much often my tables and indexes are read from cache?
    - what cache hit ratio of my queries?
    - how much temporary IO is produced by queries?
    - how much local IO is produced by queries?


7. [Shared Buffers](https://pgstats.dev/Shared%20Buffers)
    - what is shared buffers?
    - how much of shared buffers are used?
    - what tables and indexes are in the shared buffers?
    - how much space allocated by internal structures in the shared buffers?


8. [SLRU Caches](https://pgstats.dev/SLRU%20Caches)
    - what is SLRU cache?
    

9. [Server configuration]()
    - how Postgres server is configured?
    - how to list all configuration settings?
    - how to check for unapplied settings?
    - how to list all HBA rules?
    - how to change settings?
    - how to check when configuration was applied?


10. [Postmaster](https://pgstats.dev/Postmaster)
    - what is Postmaster?


11. [Background Workers](https://pgstats.dev/Background%20Workers)
    - what is background workers?
    - how many bg workers are running (for particular pid)?


12. [Autovacuum Launcher](https://pgstats.dev/Autovacuum%20Launcher)
    - what is autovacuum launcher?
    - what about wraparound?


13. [Autovacuum Workers](https://pgstats.dev/Autovacuum%20Workers)
    - what is autovacuum workers?
    - how many (auto)vacuum workers are running?
    - how long vacuum workers are executed?
    - what the progress of vacuum?
    - what the progress of running analyze commands?
    - what tables have to be vacuumed or analyzed?
    - how far autovacuum had on table?


14. [Write-Ahead Log](https://pgstats.dev/Write-Ahead%20Log)
    - what is Write-Ahead Log?
    - how to calculate distance between two WAL locations?
    - how to understand current state of WAL?
    - how many WAL are generated by server?
    - how many FPW are performed by server?
    - how to count number of WAL segments and its size?
    - how to find the most fresh standby server?


15. [Logger Process](https://pgstats.dev/Write-Ahead%20Log)
    - what is logger process?
    - what the current logfile and where is it?
    - how much size log files take?


16. [Stats Collector](https://pgstats.dev/Stats%20Collector)
    - what is stats collector?
    - why there is nothing about stats collector?

17. [Logical Replication](https://pgstats.dev/Logical%0AReplication)
    - what is logical replication?
    - how many replication slots are opened?
    - what the status of subscriptions?


18. [WAL Sender Process](https://pgstats.dev/WAL%20Sender%0AProcess)
    - what is WAL sender process?
    - how many standbys are connected to server?
    - how far connected standbys are left behind of master?


19. [WAL Archiver Process](https://pgstats.dev/WAL%20Archiver%0AProcess)
    - what is WAL archiver?
    - what the status of WAL archiver?
    - how much WAL segments are not archived?


20. [Background Writer Process](https://pgstats.dev/Background%0AWriter)
    - what is background writer?
    - how much amount of data written by bgwriter?
    - how much amount of data written by backends?
    - how often bgwriter has to forced to stop? 


21. [Checkpointer Process](https://pgstats.dev/Checkpointer%0AProcess)
    - what is checkpointer?
    - how much time are spent on write and sync phases?
    - how much amount of data written by checkpointer?


22. [Network](https://pgstats.dev/Network)
    - how network is used in cluster topology?


23. [WAL Receiver Process](https://pgstats.dev/WAL%20Receiver%20Process)
    - what is wal receiver process?
    - how much data recevied by wal receiver?


24. [Recovery Process](https://pgstats.dev/Recovery%20Process)
    - what is recovery process?
    - what the latest WAL location or transaction is replayed?
    - what is the state of recovery?


25. [Storage](https://pgstats.dev/Storage)
    - how storage is used by Postgres server?
    - where Postgres stores its data (WAL, logs, TS, etc)?


26. [Tables and Indexes Data Files](https://pgstats.dev/Tables%2FIndexes%20Data%20Files)
    - what the size of my Postgres?
    - what the size of my databases?
    - what the size of my tables?
    - what the size of my indexes?
    - what the size of temporary files?
