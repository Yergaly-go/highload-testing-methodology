# Database Testing

Нужно различать slow SQL и slow transaction.

Транзакция может быть медленной даже если каждый SQL выполняется быстро.

## Возможные причины

- большое число round trips;
- несколько transaction scopes;
- lock waiting;
- WAL/fsync;
- application work между queries;
- network latency;
- pool acquisition.

## PostgreSQL Metrics

- connections;
- pool usage;
- active backends;
- idle-in-transaction;
- transaction duration;
- lock waits;
- deadlocks;
- query latency;
- WAL writes;
- WAL syncs;
- checkpoints;
- disk I/O;
- temp files;
- rollback count.

## Transaction Map

```text
BEGIN
→ SQL
→ SQL
→ SQL
→ COMMIT
```

Для каждого этапа измеряется duration, query count, round trips, locks, commits и WAL activity.
