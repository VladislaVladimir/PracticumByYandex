**Статус проекта** - *завершен*

# Определение перспективного тарифа для телеком-компании

## Данные

В нашем распоряжении данные 500 пользователей телеком-компании: кто они, откуда, каким тарифом пользуются, сколько звонков и сообщений каждый отправил за 2018 год. 

В распоряжении 5 датасетов каждый из которых содержит:

1) Информацию о звонках. Содержит 4 столбца:

- id — уникальный номер звонка. Тип данных: object
- call_date — дата звонка. Тип данных: object
- duration — длительность звонка в минутах. Тип данных: float64
- user_id — идентификатор пользователя, сделавшего звонок. Тип данных: int64

2) Информацию об интернет-сессиях. Содержит 4 столбца:

- id — уникальный номер сессии. Тип данных: object
- mb_used — объём потраченного за сессию интернет-трафика (в мегабайтах). Тип данных: float64
- session_date — дата интернет-сессии. Тип данных: object
- user_id — идентификатор пользователя. Тип данных: int64

3) Информацию о сообщениях. Содержит 3 столбца:

- id — уникальный номер сообщения. Тип данных: object
- message_date — дата сообщения. Тип данных: object
- user_id — идентификатор пользователя, отправившего сообщение. Тип данных: int64

4) Информацию о тарифах. Содержит 8 столбцов:

- tariff_name — название тарифа. Тип данных: object
- rub_monthly_fee — ежемесячная абонентская плата в рублях. Тип данных: int64
- minutes_included — количество минут разговора в месяц, включённых в абонентскую плату. Тип данных: int64
- messages_included — количество сообщений в месяц, включённых в абонентскую плату. Тип данных: int64
- mb_per_month_included — объём интернет-трафика, включённого в абонентскую плату (в мегабайтах). Тип данных: int64
- rub_per_minute — стоимость минуты разговора сверх тарифного пакета (например, если в тарифе 100 минут разговора в месяц, то со 101 минуты будет взиматься плата). Тип данных: int64
- rub_per_message — стоимость отправки сообщения сверх тарифного пакета. Тип данных: int64
- rub_per_gb — стоимость дополнительного гигабайта интернет-трафика сверх тарифного пакета (1 гигабайт = 1024 мегабайта). Тип данных: int64
 
5) Информацию о пользователях. Содержит 8 столбцов:

- user_id — уникальный идентификатор пользователя. Тип данных: int64
- first_name — имя пользователя. Тип данных: object
- last_name — фамилия пользователя. Тип данных: object
- age — возраст пользователя (годы). Тип данных: int64
- reg_date — дата подключения тарифа (день, месяц, год). Тип данных: object
- churn_date — дата прекращения пользования тарифом (если значение пропущено, то тариф ещё действовал на момент выгрузки данных). Тип данных: object
- city — город проживания пользователя. Тип данных: object
- tarif — название тарифного плана. Тип данных: object

## Задача

Перед нами стоит задача исследования использования тарифов на выборке клиентов с целью определения перспективного тарифа для телеком-комании. А так же, проверить гипотезы о различии выручки абонентов разных тарифов и различии выручки абонентов из Москвы и других регионов.

## Используемые библиотеки

*Pandas, Matplotlib, SeaBorn, NumPy, SciPy*

# Ключевые выводы проекта

1. Тариф ультра приносит больше прибыли для компании.

2. Рекламные кампании выгоднее акцентировать на тарифе ультра.

3. Средние выручки по тарифам сильно разнятся.

4. Выручка Московского региона и других регионов одинакова.
