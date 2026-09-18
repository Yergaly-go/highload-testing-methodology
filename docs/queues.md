# Queues and Outbox Testing

Недостаточно измерять только размер очереди.

## Ключевые метрики

```text
arrival rate
processing rate
pending count
oldest message age
retry count
dead-letter count
recovery time
```

Критический критерий:

```text
processing_rate >= arrival_rate
```

на устойчивом рабочем профиле.

## Queue Predictability

Проверяется:

- data loss = 0;
- duplicate side effects = 0;
- ordering contract;
- retry contract;
- dead-letter behavior;
- stale processing recovery;
- bounded queue latency.

## Background Jobs

Рекомендуемая state model:

```text
pending
→ processing
→ completed
```

При сбое worker:

```text
processing
→ stale
→ retry/reclaim
```
