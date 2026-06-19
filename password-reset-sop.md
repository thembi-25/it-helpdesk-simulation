# SOP: Password Reset & Account Unlock
**SOP ID:** SOP-001 | **Category:** Account Access | **Priority:** P2 – High  
**Author:** Ernestina Thembi Zah | **Last Updated:** 2024-01-01 | **Version:** 1.0

---

## Purpose
Provide a consistent, secure, and auditable procedure for resetting user passwords and unlocking accounts, ensuring users regain access within SLA targets while maintaining security compliance.

## Scope
Applies to all employee account access issues including: forgotten passwords, locked accounts, MFA device changes, and temporary access requests.

## SLA Target
| Priority | Target Resolution |
|---|---|
| P2 – High (lockout affecting work) | Within 4 hours |
| P3 – Medium (non-urgent reset) | Within 8 hours |

---

## Step-by-Step Procedure

### 1. Ticket Receipt & Verification (0–5 minutes)
- [ ] Log ticket in helpdesk system with category: `Account Access`
- [ ] Verify requestor identity via **two** of the following:
  - Employee ID number
  - Manager's name
  - Last 4 digits of employee phone on file
  - Answer to security question on file
- [ ] **Do NOT proceed** if identity cannot be verified — escalate to IT Security

### 2. Diagnose Account Status (5–10 minutes)
- [ ] Open Active Directory / Identity Provider (Okta / Azure AD)
- [ ] Search for user account by email or employee ID
- [ ] Check account status:
  - `Disabled` → Escalate to HR (may be intentional)
  - `Locked` → Proceed to Step 3
  - `Active` → Check MFA status; proceed to Step 4 if MFA issue

### 3. Account Unlock (10–15 minutes)
- [ ] Right-click account in Active Directory → "Unlock Account"
- [ ] Reset password to temporary value: `[FirstName]@[Year]!Temp` (e.g. `Ernestina@2024!Temp`)
- [ ] Tick "User must change password at next logon"
- [ ] Document action in ticket: timestamp, admin account used, new temp password (masked)

### 4. MFA Reset (if applicable)
- [ ] Navigate to user's MFA settings in Okta/Microsoft Authenticator admin
- [ ] Select "Reset Authenticator" — this deregisters all existing MFA devices
- [ ] Notify user: they will need to re-enroll on next login
- [ ] Send user the MFA enrollment guide (attach `docs/mfa-enrollment-guide.pdf`)

### 5. User Notification
Send the following to user's secondary email (personal on file) or via Teams message from manager:

> Hi [Name], your account has been unlocked. Temporary password: `[TempPassword]`. You will be prompted to change it on first login. If you encounter any issues, reply to this ticket or call the helpdesk at ext. 100.

### 6. Ticket Resolution
- [ ] Update ticket status to `Resolved`
- [ ] Log resolution time
- [ ] Tag: `FCR: Yes` if resolved in single contact, `FCR: No` if required follow-up
- [ ] Send CSAT survey link to user

---

## Escalation Paths
| Scenario | Escalate To | Timeframe |
|---|---|---|
| Identity cannot be verified | IT Security team | Immediately |
| Account disabled (not locked) | HR + IT Security | Within 1 hour |
| Repeated lockouts (>3 in 30 days) | Security Operations | Same day |
| VIP / executive account | Senior IT + direct call | Within 30 mins |

## Common Issues & Fixes
| Issue | Fix |
|---|---|
| User locked out again immediately | Check for cached credentials on device (Windows Credential Manager) |
| MFA app not working after reset | Ensure user deletes OLD account in authenticator app before re-enrolling |
| Temp password rejected | Check password policy — minimum 10 chars, 1 uppercase, 1 number, 1 symbol |

## Related SOPs
- SOP-002: New Employee IT Onboarding
- SOP-004: VPN Troubleshooting
- SOP-006: Security Incident Response

---
*Reviewed and approved for use. Questions: helpdesk@company.com*
