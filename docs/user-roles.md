\# FORECAST AI User Roles



\## User



A registered user who manages personal financial data.



\### Permissions



\- Register account

\- Login

\- Update profile

\- Add salary details

\- Edit salary records

\- Add expenses

\- Delete expenses

\- View forecasts

\- Calculate taxes

\- Download reports

\- View dashboard



\---



\## Admin



Administrator responsible for system management.



\### Permissions



\- View all users

\- Manage users

\- Update tax rules

\- Monitor forecasts

\- Access analytics

\- View system logs

\- Manage reports



\## Permission Matrix



| Feature | User | Admin |

|----------|------|-------|

| Register | Yes | Yes |

| Login | Yes | Yes |

| Add Salary | Yes | Yes |

| Add Expense | Yes | Yes |

| View Dashboard | Yes | Yes |

| Generate Forecast | Yes | Yes |

| Calculate Tax | Yes | Yes |

| View All Users | No | Yes |

| Update Tax Rules | No | Yes |

| View Analytics | No | Yes |



\## Role Storage



User roles will be stored in the users table.



Example:



user\_id

name

email

role



Possible values:



USER

ADMIN



\## Authentication Flow



Register

&#x20;   ↓

Login

&#x20;   ↓

JWT Token

&#x20;   ↓

Role Validation

&#x20;   ↓

Access Features



\## Future Admin Features



\- Manage tax slabs

\- View user growth

\- View revenue analytics

\- Manage notifications

\- View AI model performance





