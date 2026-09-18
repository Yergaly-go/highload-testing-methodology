# Generic Load Profile Example

Пример универсального профиля нагрузки без раскрытия реальных production limits.

| Stage | Duration | Users | Goal |
|---|---:|---:|---|
| Warm-up | 5 min | 50 | Прогрев системы |
| Baseline | 10 min | 100 | Стабильная точка сравнения |
| Normal load | 20 min | 500 | Рабочая нагрузка |
| Peak load | 10 min | 1500 | Пиковая нагрузка |
| Stress | 10 min | 3000+ | Поиск предела |
| Cool-down | 5 min | 50 | Стабилизация |

## Важно

Количество пользователей и RPS нужно тестировать отдельно.

```text
concurrent users != RPS
```

Реальные лимиты, tenant counts, customer data и production capacity не публикуются.
