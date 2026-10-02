# NexG-User-Access-Review

GRC portfolio project demonstrating a User Access Review control assessment using Microsoft Entra ID.

# User Access Review & Remediation Control Assessment



## Scope

This assessment covers the User Access Review control for **NexG Services Ltd**, a fictional organization with 15 employees, limited to user accounts and memberships within **Microsoft Entra ID**. A separate administrative account is used for tenant administration, which is excluded from the employee review.

The assessment evaluates whether access matches employees' current responsibilities and is appropriately adjusted following role changes or departure.


---

## Control Objective

The objective of the User Access Review control is to ensure that user access is authorized, appropriate and aligns with employees' current job responsibilities.

This includes:

- Users receive only the access required to perform their assigned duties.
- Excessive or inappropriate access is identified and removed.
- Access is updated when an employee's role or department changes.
- Access is removed when an employee leaves the organization.
- Evidence of the review, identified exceptions, approvals and remediation actions are retained.

---

## Framework Mapping

| Focus | Framework Mapping | Failure |
|---|---|---|
| **User access appropriateness** | NIST CSF 2.0 PR.AA-05 | Employees retain access beyond their current responsibilities because access permissions are not adequately reviewed against their assigned roles. |
| **Access following role changes** | ISO/IEC 27001:2022 A.5.18 & NIST CSF 2.0 PR.AA-05 | Employees retain outdated access after changing departments because access rights are not reviewed and modified following changes in responsibilities. |
| **Access removal** | ISO/IEC 27001:2022 A.5.18 & NIST CSF 2.0 PR.AA-05 | Departed personnel retain access because offboarding does not trigger timely review and revocation of their access rights. |

---

## Testing Methodology

1. Identify the user accounts in Microsoft Entra ID.
2. Identify each employee's current role, department and employment status.
3. Establish the expected responsibilities and status.
4. Review the group memberships in Entra ID.
5. Compare the expected access to the current access.
6. Identify findings.
7. Confirm findings.
8. Document findings.
9. Remediate exceptions by removing, modifying or disabling access.
10. Retest the affected accounts.
11. Document the conclusion.

---

## Evidence to be Collected

1. Microsoft Entra ID user accounts (https://github.com/KD-J30/NexG-User-Access-Review/blob/main/Employeeslist.md)
2. Microsoft Entra ID groups (https://github.com/KD-J30/NexG-User-Access-Review/blob/main/Employeeslist.md) 
3. User group memberships and access rights (https://github.com/KD-J30/NexG-User-Access-Review/blob/main/Employeeslist.md)
4. Expected vs actual access (https://github.com/KD-J30/NexG-User-Access-Review/blob/main/Employeeslist.md)
5. Account status (https://github.com/KD-J30/NexG-User-Access-Review/blob/main/Employeeslist.md)
6. Identified access exceptions
7. Remediation actions
8. Post-remediation access status
9. Retest evidence

---

# Findings

## 1. Unnecessary Access

- **Employee:** Sarah Adams
- **Role:** Accountant
- **Department:** Finance
- **Expected Access:** Finance
- **Actual Access:** Finance and Marketing

Sarah Adams had Marketing access in addition to her required Finance access.

### Evidence — Initial Access

The following evidence demonstrates the access identified during the initial review.



![Sarah Adams Initial Access](https://github.com/KD-J30/NexG-User-Access-Review/blob/main/Evidence%20for%20NexG/Sarah%20adams/Screenshot%202026-10-02%20232628.png)

---

## 2. Access Not Updated After Department Transfer

- **Employee:** Daniel Evans
- **Former Role:** IT Support
- **New Role:** Sales Executive
- **New Department:** Sales
- **Expected Access:** Sales
- **Actual Access:** IT

Daniel Evans retained his previous IT access after transferring to the Sales department.

### Evidence — Initial Access

The following evidence demonstrates the access identified during the initial review.



![Daniel Evans Initial Access](https://github.com/KD-J30/NexG-User-Access-Review/blob/main/Evidence%20for%20NexG/Daniel/Screenshot%202026-10-02%20232708.png)

---

## 3. Active Access Following Employee Resignation

- **Employee:** Emma Wilson
- **Previous Role:** Marketing Officer
- **Department:** Marketing
- **Employee Status:** Resigned
- **Expected Access:** No access
- **Actual Access:** Active Microsoft Entra account and membership in Marketing

Emma Wilson's Microsoft Entra account remained active and retained Marketing membership despite her resignation.

### Evidence — Initial Access

The following evidence demonstrates the active account and Marketing membership identified during the initial review.



![Emma Wilson Initial Access](https://github.com/KD-J30/NexG-User-Access-Review/blob/main/Evidence%20for%20NexG/Emma/Screenshot%202026-09-21%20110520.png) 


![Emma Wilson Initial Access](https://github.com/KD-J30/NexG-User-Access-Review/blob/main/Evidence%20for%20NexG/Emma/Screenshot%202026-09-21%20185518.png)


---

# Executions

| Task Performed | Action Taken |
|---|---|
| Reviewed employee roles and Microsoft Entra ID access permissions | Identified excessive access and recorded the exception for remediation. |
| Reviewed access for an employee following a department change | Removed outdated access and updated group membership to match the employee's new responsibilities. |
| Reviewed Microsoft Entra ID access for a departed employee | Disabled the account and removed associated access rights. |
| Retested remediated accounts | Confirmed that identified access exceptions were resolved. |

---

# Post-Remediation Evidence

The following evidence demonstrates that the identified access-management exceptions were remediated.

## Sarah Adams — Unnecessary Access Removed

The unnecessary Marketing access was removed, leaving Sarah Adams with the required Finance access.

![Sarah Adams Remediation](https://github.com/KD-J30/NexG-User-Access-Review/blob/main/Evidence%20for%20NexG/Sarah%20adams/Screenshot%202026-10-02%20233312.png)

---

## Daniel Evans — Access Updated Following Department Transfer

Daniel Evans' outdated IT access was removed and his access was updated to reflect his new Sales responsibilities.

![Daniel Evans Remediation](https://github.com/KD-J30/NexG-User-Access-Review/blob/main/Evidence%20for%20NexG/Daniel/Screenshot%202026-10-02%20233327.png)

---

## Emma Wilson — Access Removed Following Employee Resignation

Emma Wilson's account was disabled and associated organizational access was removed following her resignation.

![Emma Wilson Remediation](https://github.com/KD-J30/NexG-User-Access-Review/blob/main/Evidence%20for%20NexG/Emma/Screenshot%202026-09-21%20125950.png)

![Emma Wilson Remediation](https://github.com/KD-J30/NexG-User-Access-Review/blob/main/Evidence%20for%20NexG/Emma/Screenshot%202026-09-21%20185633.png)

---

# Recommendations

## 1. Quarterly Access Recertification

Implement a quarterly access recertification process where department managers confirm each employee's group memberships are still appropriate.

## 2. Access Review Following Role Changes

Integrate department transfers with a mandatory access review step, so access is re-evaluated whenever an employee's role changes in HR records.

## 3. Automated Deprovisioning

Automate deprovisioning by linking employee termination in HR to immediate account disablement and group removal in Microsoft Entra ID, rather than relying on manual offboarding steps.

---

# Conclusion

Based on the testing performed and evidence obtained, three access-management exceptions were identified across the 15 employees reviewed, representing a **20% exception rate**. The exceptions included unnecessary access, outdated access following a department transfer and an active account belonging to an employee who had already left the organization. Although all three exceptions were remediated, their identification indicates that the access-management process at **NexG Services Ltd** was not operating properly to ensure that user access remained appropriate and up to date. 

