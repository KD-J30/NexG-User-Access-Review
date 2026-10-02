
## Excel Spreadsheet

[ Download Excel Spreadsheet](https://github.com/KD-J30/NexG-User-Access-Review/raw/refs/heads/main/NexG%20Services%20Ltd/NexG%20Services%20Ltd.xlsx)

## Employees & Expected Access

| Employee ID | Name | Department | Job Title | Status | Expected Access |
|---|---|---|---|---|---|
| EMP001 | Sarah Adams | Finance | Accountant | Active | Finance |
| EMP002 | John Brown | Finance | Finance Manager | Active | Finance |
| EMP003 | Emily Carter | HR | HR Officer | Active | HR |
| EMP004 | Michael Davis | HR | HR Manager | Active | HR |
| EMP005 | Daniel Evans | Sales | Sales Executive | Active | Sales |
| EMP006 | Olivia Foster | IT | IT Administrator | Active | IT |
| EMP007 | James Green | Sales | Sales Executive | Active | Sales |
| EMP008 | Sophia Harris | Sales | Sales Manager | Active | Sales |
| EMP009 | William Jones | Marketing | Marketing Officer | Active | Marketing |
| EMP010 | Ava Lewis | Marketing | Marketing Manager | Active | Marketing |
| EMP011 | Noah Martin | Operations | Operations Officer | Active | Operations |
| EMP012 | Mia Nelson | Operations | Operations Manager | Active | Operations |
| EMP013 | Ethan Parker | Management | Managing Director | Active | Management |
| EMP014 | Isabella Roberts | Legal | Legal Officer | Active | Legal |
| EMP015 | Emma Wilson | - | - | Inactive | No Access |




## Administrative Lab Account

The Microsoft Entra ID tenant contains one separate administrative account used to create and administer the fictional lab environment.

| Account | Purpose | Scope | Reason |
|---|---|---|---|
| K J | Tenant administration  | Out of Scope | Administrative account used to manage the environment (not part of the 15-employee population) |




## Pre Remediation Access Review

| Employee | Role / Status | Expected Access | Actual Access | Result | Notes |
|---|---|---|---|---|---|
| Sarah Adams | Accountant | Finance | Finance + Marketing | Fail | Marketing access not required |
| John Brown | Finance Manager | Finance | Finance | Pass | Appropriate |
| Emily Carter | HR Officer | HR | HR | Pass | Appropriate |
| Michael Davis | HR Manager | HR | HR | Pass | Appropriate |
| Daniel Evans | Sales Executive | Sales | IT | Fail | Access not updated after department transfer |
| Olivia Foster | IT Administrator | IT | IT | Pass | Appropriate |
| James Green | Sales Executive | Sales | Sales | Pass | Appropriate |
| Sophia Harris | Sales Manager | Sales | Sales | Pass | Appropriate |
| William Jones | Marketing Officer | Marketing | Marketing | Pass | Appropriate |
| Ava Lewis | Marketing Manager | Marketing | Marketing | Pass | Appropriate |
| Noah Martin | Operations Officer | Operations | Operations | Pass | Appropriate |
| Mia Nelson | Operations Manager | Operations | Operations | Pass | Appropriate |
| Ethan Parker | Managing Director | Management | Management | Pass | Appropriate |
| Isabella Roberts | Legal Officer | Legal | Legal | Pass | Appropriate |
| Emma Wilson | Former Marketing Officer | No access | Marketing | Fail | Employee has left the organization |

## Evidence

### 1. Employee Evidence

![Employee Evidence 1](https://github.com/KD-J30/NexG-User-Access-Review/blob/main/NexG%20Services%20Ltd/Evidence/Group%20and%20user%20evidence/Screenshot%202026-09-21%20105744.png?raw=true)

![Employee Evidence 2](https://github.com/KD-J30/NexG-User-Access-Review/blob/main/NexG%20Services%20Ltd/Evidence/Group%20and%20user%20evidence/Screenshot%202026-09-21%20105807.png?raw=true)

### 2. Group Evidence

![Group Evidence 1](https://github.com/KD-J30/NexG-User-Access-Review/blob/main/NexG%20Services%20Ltd/Evidence/Group%20and%20user%20evidence/Screenshot%202026-09-21%20105932.png?raw=true)
