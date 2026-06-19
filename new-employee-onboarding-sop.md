# SOP: New Employee IT Onboarding
**SOP ID:** SOP-002 | **Category:** Onboarding | **Priority:** P2 – High  
**Author:** Ernestina Thembi Zah | **Last Updated:** 2024-01-01 | **Version:** 1.0

---

## Purpose
Ensure every new employee has all required IT access, hardware, and software configured and ready on or before their first day, enabling a productive start without IT delays.

## Scope
All new full-time employees, contractors, and interns requiring IT access. HR must submit onboarding request minimum **5 business days** before start date.

## SLA Target
All items below completed **by 9:00 AM on the employee's first day.**

---

## Pre-Arrival Checklist (5 Days Before Start)

### Day -5: HR Notification Received
- [ ] Receive completed New Hire IT Request form from HR
- [ ] Confirm: full name, job title, department, manager, start date, office location, remote/hybrid status
- [ ] Log onboarding ticket: `TKT-ONBOARD-[EmployeeID]`
- [ ] Order hardware if required (laptop, monitor, peripherals) — allow 3–5 days for delivery

### Day -3: Account Creation
- [ ] Create Active Directory account: `[firstname].[lastname]@company.com`
- [ ] Set initial password per policy, flag for change on first login
- [ ] Assign to appropriate security groups based on department (see `docs/department-access-matrix.xlsx`)
- [ ] Create Microsoft 365 / Google Workspace account
- [ ] Add to department distribution lists and Teams/Slack channels
- [ ] Set up MFA — send enrollment email to personal address on file

### Day -1: Hardware & Software Setup
- [ ] Unbox and asset-tag device: log serial number and asset tag in `tracker/asset-inventory.xlsx`
- [ ] Enroll device in MDM (Microsoft Intune / Jamf)
- [ ] Install required software from department software list:
  - [ ] Endpoint protection (CrowdStrike / Windows Defender)
  - [ ] VPN client (configured and tested)
  - [ ] Department-specific tools (see department matrix)
  - [ ] Collaboration: Teams / Slack / Zoom
  - [ ] Browser + extensions
- [ ] Test login with new credentials on the physical device
- [ ] Test VPN connectivity (if remote/hybrid employee)
- [ ] Confirm email is receiving messages (send test email)

---

## Day 1: Employee Walkthrough (30 Minutes)

Conduct via video call (remote) or in-person. Cover:

- [ ] **Login & password change** — walk user through changing temp password
- [ ] **MFA enrollment** — guide through authenticator app setup
- [ ] **Email & calendar** — show inbox, calendar sharing, meeting scheduling
- [ ] **File storage** — OneDrive/Google Drive structure for department
- [ ] **VPN** — demonstrate connect/disconnect, when to use
- [ ] **Key contacts** — helpdesk email, ext., self-service portal URL
- [ ] **Acceptable use policy** — confirm employee has read and acknowledge in ticket

Close with:
> "If you have any IT questions today or this week, email helpdesk@company.com or call ext. 100. We typically respond within 4 hours."

---

## Post-Onboarding (Day 3–5 Check-In)
- [ ] Send brief check-in message: "How is everything working? Any IT issues?"
- [ ] Confirm no access issues have emerged
- [ ] Update ticket status to `Closed`
- [ ] Record CSAT

## Asset Tracking
All hardware issued must be logged in `tracker/asset-inventory.xlsx`:

| Field | Example |
|---|---|
| Asset Tag | AT-2024-0042 |
| Device Type | Laptop |
| Make/Model | Dell Latitude 5540 |
| Serial Number | ABC123XYZ |
| Assigned To | Ernestina Zah |
| Department | IT Support |
| Date Issued | 2024-03-15 |
| Condition | New |

## Escalation
| Scenario | Action |
|---|---|
| Hardware not arrived by Day -1 | Alert manager + HR; arrange loaner |
| Software licence unavailable | Request emergency licence from IT Manager |
| Employee cannot log in on Day 1 | Immediate P1 priority; resolve within 1 hour |

## Related SOPs
- SOP-001: Password Reset & Account Unlock
- SOP-003: Employee Offboarding
- SOP-004: VPN Troubleshooting
