# Список триггеров для таблицы PostponesTable

### 1. Проверка дат

Срабатывание: BEFORE UPDATE/INSERT

Действия: Проверка на то, чтобы новая дата вылета была позже старой дат вылета. Если нет, выбрасывается исключение
