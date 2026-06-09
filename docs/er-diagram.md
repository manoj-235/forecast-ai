\# FORECAST AI ER Diagram



User

&#x20;↓

Tax Profile



User

&#x20;↓

Expenses



Students

&#x20;↓

Courses



User → Salaries

User → Expenses

User → Budgets

User → Forecasts

User → Reports

User → Notifications

User → Tax Profiles



One User

&#x20;     ↓

Many Records



USERS

&#x20; |

&#x20; +---- SALARIES

&#x20; |

&#x20; +---- EXPENSES

&#x20; |

&#x20; +---- BUDGETS

&#x20; |

&#x20; +---- FORECASTS

&#x20; |

&#x20; +---- TAX\_PROFILES

&#x20; |

&#x20; +---- REPORTS

&#x20; |

&#x20; +---- NOTIFICATIONS



EXPENSE\_CATEGORIES

&#x20;         |

&#x20;         |

&#x20;         +---- EXPENSES



EXPENSE\_CATEGORIES

&#x20;       |

&#x20;       +---- BUDGETS



USERS

&#x20;|

&#x20;+---- SALARIES

&#x20;|

&#x20;+---- EXPENSES

&#x20;|          |

&#x20;|          |

&#x20;|          +---- EXPENSE\_CATEGORIES

&#x20;|

&#x20;+---- BUDGETS

&#x20;|          |

&#x20;|          |

&#x20;|          +---- EXPENSE\_CATEGORIES

&#x20;|

&#x20;+---- FORECASTS

&#x20;|

&#x20;+---- TAX\_PROFILES

&#x20;|

&#x20;+---- REPORTS

&#x20;|

&#x20;+---- NOTIFICATIONS



\## Foreign Keys



| Child Table   | Foreign Key | Parent Table       |

| ------------- | ----------- | ------------------ |

| salaries      | user\_id     | users              |

| expenses      | user\_id     | users              |

| expenses      | category\_id | expense\_categories |

| budgets       | user\_id     | users              |

| budgets       | category\_id | expense\_categories |

| forecasts     | user\_id     | users              |

| tax\_profiles  | user\_id     | users              |

| reports       | user\_id     | users              |

| notifications | user\_id     | users              |



\## Relationship Summary



| Parent             | Child         | Type |

| ------------------ | ------------- | ---- |

| Users              | Salaries      | 1:N  |

| Users              | Expenses      | 1:N  |

| Users              | Budgets       | 1:N  |

| Users              | Forecasts     | 1:N  |

| Users              | Reports       | 1:N  |

| Users              | Notifications | 1:N  |

| Users              | Tax Profiles  | 1:1  |

| Expense Categories | Expenses      | 1:N  |

| Expense Categories | Budgets       | 1:N  |



+-----------+

|   USERS   |

+-----------+

&#x20;     |

&#x20;     |

&#x20;     +----------------+

&#x20;     |                |

&#x20;     v                v

+-----------+   +-------------+

| SALARIES  |   |  EXPENSES   |

+-----------+   +-------------+

&#x20;                   |

&#x20;                   |

&#x20;                   v

&#x20;         +--------------------+

&#x20;         | EXPENSE\_CATEGORIES |

&#x20;         +--------------------+



&#x20;     |

&#x20;     |

&#x20;     v



+-----------+

| BUDGETS   |

+-----------+

&#x20;     |

&#x20;     |

&#x20;     v



+--------------------+

| EXPENSE\_CATEGORIES |

+--------------------+



&#x20;     |

&#x20;     |

&#x20;     +------------------+

&#x20;     |        |         |

&#x20;     v        v         v



+-----------+ +--------+ +---------------+

|FORECASTS  | |REPORTS | |NOTIFICATIONS  |

+-----------+ +--------+ +---------------+



&#x20;     |

&#x20;     v



+--------------+

| TAX\_PROFILES |

+--------------+

