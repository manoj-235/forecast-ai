\# FORECAST AI Database Design



\## Core Entities



1\. Users

2\. Salaries

3\. Expenses

4\. Expense Categories

5\. Budgets

6\. Forecasts

7\. Tax Profiles

8\. Reports

9\. Notifications



\## Users Table



| Field      | Type         | Description       |

| ---------- | ------------ | ----------------- |

| id         | UUID         | Primary Key       |

| name       | VARCHAR(100) | User Name         |

| email      | VARCHAR(255) | Unique Email      |

| password   | VARCHAR(255) | Hashed Password   |

| role       | VARCHAR(20)  | USER/ADMIN        |

| created\_at | TIMESTAMP    | Registration Date |



users

\------

id

name

email

password

role

created\_at



\## Salaries Table



| Field        | Type      |

| ------------ | --------- |

| salary\_id    | UUID      |

| user\_id      | UUID      |

| gross\_salary | DECIMAL   |

| net\_salary   | DECIMAL   |

| bonus        | DECIMAL   |

| month        | INTEGER   |

| year         | INTEGER   |

| created\_at   | TIMESTAMP |





\## Expenses Table



| Field        | Type      |

| ------------ | --------- |

| expense\_id   | UUID      |

| user\_id      | UUID      |

| category\_id  | UUID      |

| amount       | DECIMAL   |

| description  | TEXT      |

| expense\_date | DATE      |

| created\_at   | TIMESTAMP |





\## Expense Categories Table



| Field         | Type         |

| ------------- | ------------ |

| category\_id   | UUID         |

| category\_name | VARCHAR(100) |



\## Budget Table



| Field         | Type    |

| ------------- | ------- |

| budget\_id     | UUID    |

| user\_id       | UUID    |

| category\_id   | UUID    |

| budget\_amount | DECIMAL |

| month         | INTEGER |

| year          | INTEGER |



\## Forecast Table



| Field            | Type      |

| ---------------- | --------- |

| forecast\_id      | UUID      |

| user\_id          | UUID      |

| forecast\_type    | VARCHAR   |

| predicted\_amount | DECIMAL   |

| forecast\_month   | INTEGER   |

| forecast\_year    | INTEGER   |

| generated\_at     | TIMESTAMP |



\## Tax Profiles Table



| Field          | Type    |

| -------------- | ------- |

| tax\_profile\_id | UUID    |

| user\_id        | UUID    |

| tax\_regime     | VARCHAR |

| annual\_income  | DECIMAL |

| deductions     | DECIMAL |

| tax\_payable    | DECIMAL |

| financial\_year | VARCHAR |



\## Reports Table



| Field       | Type      |

| ----------- | --------- |

| report\_id   | UUID      |

| user\_id     | UUID      |

| report\_type | VARCHAR   |

| file\_path   | VARCHAR   |

| created\_at  | TIMESTAMP |



\## Notifications Table



| Field           | Type      |

| --------------- | --------- |

| notification\_id | UUID      |

| user\_id         | UUID      |

| title           | VARCHAR   |

| message         | TEXT      |

| is\_read         | BOOLEAN   |

| created\_at      | TIMESTAMP |



\## Relationships



Users

&#x20;|

&#x20;+---- Salaries

&#x20;|

&#x20;+---- Expenses

&#x20;|

&#x20;+---- Budgets

&#x20;|

&#x20;+---- Forecasts

&#x20;|

&#x20;+---- Tax Profiles

&#x20;|

&#x20;+---- Reports

&#x20;|

&#x20;+---- Notifications



Expense Categories

&#x20;|

&#x20;+---- Expenses

&#x20;|

&#x20;+---- Budgets



\## Future Enhancements



Bank Accounts

Transactions

Investments

AI Chat History

Audit Logs







