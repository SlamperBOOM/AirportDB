# Список триггеров для таблицы Passengers

### 1. Добавление проданного билета в таблицу FlightsTable

Срабатывание: AFTER INSERT

Действия: У нужного рейса увеличивается количество проданных билетов на 1

### 2. Изменение проданных билетов

Срабатывание: AFTER UPDATE

Действия: У старого рейса уменьшается количество проданных билетов на 1, у нового рейса увеличивается на 1. Если старый и новый рейс совпадают, то никаких действий не выполняется

### 3. Удаление проданных билетов

Срабатывание: AFTER DELETE

Действия: У рейса, связанного с удаленным пассажиром, уменьшается количество проданных билетов на 1

### 4. Проверка возраста

Срабатывание: BEFORE INSERT/UPDATE

Действия: Возраст пассажира проверяется на неотрицательность. Если меньше нуля, выбрасывается исключение

### 5. Удаление проданного билета при возврате

Срабатывание: AFTER UPDATE

Действия: Если при обновлении записи добавилась дата возврата, количество проданных билетов у рейса уменьшается на 1