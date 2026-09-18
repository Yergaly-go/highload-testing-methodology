# Load Testing

Load test проверяет систему под ожидаемой рабочей нагрузкой.

## Цели

- подтвердить рабочий capacity;
- измерить latency;
- проверить background pipeline;
- оценить DB pressure;
- увидеть error rate под нормальной нагрузкой.

## Минимальный сценарий

1. Запустить smoke test.
2. Зафиксировать версию source.
3. Подготовить synthetic data.
4. Запустить baseline.
5. Увеличить нагрузку до normal profile.
6. Собрать HTTP, DB, queue и system metrics.
7. Провести correctness reconciliation.
8. Зафиксировать результат: PASS / FAIL / DEGRADED / INVALID.

## Метрики HTTP

- RPS;
- throughput;
- p50;
- p95;
- p99;
- max latency;
- 4xx;
- 5xx;
- timeouts;
- dropped iterations.
