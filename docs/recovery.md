# Failure and Recovery Testing

Создаётся контролируемый сбой и проверяется восстановление системы.

## Примеры сбоев

- restart API;
- restart worker;
- временная недоступность Redis;
- DB slowdown;
- external API timeout;
- process interruption.

## Проверяется

- теряются ли данные;
- появляются ли дубликаты;
- восстанавливаются ли jobs;
- очищается ли backlog;
- сколько занимает recovery.

## Recovery Gate

После завершения генератора нагрузки тест ещё не закончен.

Нужно дождаться:

```text
queue pending → 0
jobs processing → 0
DB pool → baseline
latency → normal
```

И измерить recovery time.
