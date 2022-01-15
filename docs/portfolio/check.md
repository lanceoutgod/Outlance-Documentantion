# Создание проверки портфолио

Проверка создается автоматически во время того, как юзер переводит портфолио из статуса "in_work" в статус "on_check".
В этот момент создаются три таблицы CheckExecutorPortfolio и таблицы CheckSkillInPortfolio, соответствующие скилам портфолио (api_v2.signals.portfolio_review_generator).

/api_v2/portfolio/{id}/ [PATCH]
### Json Example
```json
{
    "type": 0,
    "categories": [
        0
    ],
    "confirmation": "in_work" -> "on_check" !!!
}
```