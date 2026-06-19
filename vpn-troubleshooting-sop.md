# SOP: VPN Troubleshooting
**SOP ID:** SOP-004 | **Category:** Network/VPN | **Priority:** P1–P2  
**Author:** Ernestina Thembi Zah | **Last Updated:** 2024-01-01 | **Version:** 1.0

---

## Purpose
Diagnose and resolve VPN connectivity issues for remote and hybrid employees using a structured troubleshooting approach that achieves first-contact resolution wherever possible.

## Scope
All VPN-related tickets including: cannot connect, slow speeds, frequent disconnections, and split-tunnel configuration issues.

## SLA Targets
| Priority | Target |
|---|---|
| P1 – VPN down, employee cannot work | 1 hour |
| P2 – VPN intermittent, work affected | 4 hours |

---

## Diagnostic Tree

### Step 1: Confirm Scope (2 minutes)
Ask:
- "Is this affecting only you, or have colleagues reported the same issue?"
- If **multiple users affected** → likely server-side issue → escalate to Network team immediately (skip to Step 6)
- If **single user** → continue to Step 2

### Step 2: Basic Connectivity Check (5 minutes)
- [ ] Can user browse the internet without VPN? (Yes = local network is fine; No = internet issue, not VPN)
- [ ] Ask user to ping `8.8.8.8` — if no response, internet is down (ISP issue — outside helpdesk scope; advise user to contact ISP)
- [ ] Confirm VPN client version: open client → Help → About. Compare against current approved version in `docs/approved-software-versions.md`

### Step 3: VPN Client Reset (10 minutes)
- [ ] Ask user to fully quit VPN client (not just minimise — check system tray/taskbar)
- [ ] Re-open and attempt connection
- [ ] If fails: clear VPN cache:
  - **Windows**: `C:\Users\[username]\AppData\Roaming\[VPNClient]\` — delete cache folder
  - **Mac**: `~/Library/Application Support/[VPNClient]/` — delete cache folder
- [ ] Retry connection

### Step 4: Credential & MFA Check (5 minutes)
- [ ] Confirm user is entering correct credentials (same as Windows login)
- [ ] Confirm MFA is enrolled and working — ask user to open authenticator app
- [ ] If MFA code rejected: check device time sync (incorrect time causes TOTP failures)
  - Windows: `Settings → Time → Sync Now`
  - Mac: `System Preferences → Date & Time → Set automatically`

### Step 5: Reinstall VPN Client (20 minutes)
If Steps 2–4 fail:
- [ ] Download latest approved VPN client from IT intranet portal
- [ ] Uninstall existing client (Windows: Add/Remove Programs | Mac: drag to Trash + delete config files)
- [ ] Restart device
- [ ] Install fresh download
- [ ] Import configuration file (send from helpdesk if user doesn't have it)
- [ ] Test connection

### Step 6: Escalation (if Steps 1–5 fail)
- [ ] Collect: VPN client logs (Help → Export Logs), screenshot of error message, OS version
- [ ] Escalate ticket to Network Engineer with all collected info
- [ ] Update ticket: escalation time, reason, assignee
- [ ] Set user expectation: "I've escalated this to our network team. You should hear back within 2 hours."

---

## Common Error Codes & Fixes
| Error | Likely Cause | Fix |
|---|---|---|
| "Authentication failed" | Wrong password or MFA failure | Reset password (SOP-001); re-sync MFA time |
| "Connection timed out" | Firewall blocking VPN port | Check firewall allows UDP 1194 / TCP 443 |
| "TLS handshake failed" | Outdated client or certificate issue | Reinstall client; escalate if persists |
| "No network adapter found" | Driver issue | Device Manager → Network Adapters → Update driver |
| Connects but no access to resources | Split tunnel misconfiguration | Re-import config file from helpdesk |

## Ticket Documentation
Always record in ticket:
- OS version and VPN client version
- Steps taken and results of each
- Error message (exact text or screenshot)
- Resolution or escalation path

## Related SOPs
- SOP-001: Password Reset & Account Unlock
- SOP-002: New Employee IT Onboarding
