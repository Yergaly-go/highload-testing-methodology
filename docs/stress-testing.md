# Stress Testing

Stress test постепенно повышает нагрузку до появления деградации.

## Цель

Определить первый устойчивый предел системы и компонент, который первым начинает ограничивать поток.

## Подход

```text
Level 1
↓
Level 2
↓
Level 3
↓
Level 4
```

Каждый следующий уровень разрешён только после успешного предыдущего.

## Stop Conditions

До теста задаются условия аварийной остановки:

- sustained 5xx;
- deadlock;
- data corruption;
- queue age above limit;
- DB pool exhaustion;
- transaction age above limit;
- severe p99 degradation.
