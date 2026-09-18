# Correctness Reconciliation

После нагрузки необходимо сверять данные.

## Пример сверки

```text
successful API operations
=
business records
=
outbox events
=
expected projections
=
background jobs
```

## Проверяется

- lost writes;
- duplicate rows;
- orphan rows;
- tenant mismatch;
- broken references;
- incorrect aggregates.

## Idempotency

Любая операция, которая может быть повторена клиентом после timeout, должна иметь определённый retry contract.

```text
first request
→ commit
→ client loses response
→ retry
```

Результат должен быть предсказуемым.
