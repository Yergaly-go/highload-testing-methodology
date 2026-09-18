# Highload Testing Checklist

## Before Test

- [ ] Определены цели теста
- [ ] Подготовлены тестовые данные
- [ ] Настроено логирование
- [ ] Настроен мониторинг
- [ ] Известны целевые SLA/SLO
- [ ] Определены критичные endpoints
- [ ] Исключены реальные персональные данные
- [ ] API keys и secrets не попадают в репозиторий
- [ ] Есть план отката
- [ ] Подготовлен отчетный шаблон
- [ ] Source freeze подтвержден
- [ ] Environment изолирован

## During Test

- [ ] Собираются HTTP metrics
- [ ] Собираются DB metrics
- [ ] Собираются queue metrics
- [ ] Собираются system metrics
- [ ] Проверяются stop conditions

## After Test

- [ ] Проведена correctness reconciliation
- [ ] Измерено recovery time
- [ ] Определён первый bottleneck
- [ ] Сформирован test report
- [ ] Зафиксирован следующий gate
