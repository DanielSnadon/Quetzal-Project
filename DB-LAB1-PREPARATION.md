```sql
-- Добавить столбец
ALTER TABLE clients
ADD COLUMN name VARCHAR(50);

-- Переименовать столбец
ALTER TABLE clients
RENAME COLUMN phone TO phone_number;

-- Изменить тип
ALTER TABLE accounts
ALTER COLUMN currency TYPE VARCHAR(3);

-- Установить значение по умолчанию
ALTER TABLE accounts
ALTER COLUMN status SET DEFAULT 'active';

-- Добавить ограничение
ALTER TABLE accounts
ADD CONSTRAINT accounts_balance_check
CHECK (balance >= 0);

-- Удалить ограничение
ALTER TABLE accounts
DROP CONSTRAINT accounts_balance_check;

-- Сделать столбец обязательным
ALTER TABLE clients
ALTER COLUMN email SET NOT NULL;
```