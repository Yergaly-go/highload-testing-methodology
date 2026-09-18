# Observability

Нагрузочное тестирование без наблюдаемости не позволяет доказать причину деградации.

## Минимально полезны

- Prometheus;
- Grafana;
- application metrics;
- PostgreSQL statistics;
- structured logs.

## Для более глубокой диагностики

- OpenTelemetry;
- distributed tracing;
- pprof;
- runtime metrics;
- pg_stat_statements.

## Performance Regression

После определения стабильного baseline желательно автоматизировать небольшой performance smoke:

```text
CI / nightly
baseline load
→ collect p95
→ collect throughput
→ compare against previous baseline
```

Если latency выросла значительно, фиксируется performance regression.
