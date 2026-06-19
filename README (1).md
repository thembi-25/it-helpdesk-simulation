# 🖥️ IT Helpdesk Simulation

> **Tools:** Python (pandas) · Microsoft Excel · SOP Documentation · KPI Dashboard Design
> **Type:** IT Support Portfolio Project
> **Author:** Ernestina Thembi Zah | [LinkedIn](https://linkedin.com/in/zahthembiernestina)

## 📌 Project Overview

A fully simulated IT helpdesk environment modelling a real-world 4-agent support team handling 320 tickets across a full year. Demonstrates systematic IT support thinking, professional documentation skills, and data-driven performance tracking.

## 📊 Simulated KPIs Achieved

| Metric | Result |
|---|---|
| Total Tickets Handled | 320 |
| First-Contact Resolution Rate | 86.9% |
| SLA Compliance Rate | 71.2% |
| Average CSAT Score | 4.25 / 5.0 |
| Resolution Rate | 93% |

## 🎯 What This Project Demonstrates

- **Systematic troubleshooting thinking** — structured diagnostic trees, not guesswork
- **Professional SOP writing** — 3 SOPs covering the most common helpdesk scenarios
- **Data tracking & reporting** — KPI dashboard built from raw ticket data
- **Escalation judgement** — documented escalation matrix with clear decision paths
- **IT tools knowledge** — Active Directory, MDM, Zendesk, MFA, VPN diagnostics

## 📋 Ticket Categories Simulated

| Category | Tickets | Notes |
|---|---|---|
| Network / VPN | 68 | Highest volume — most common remote work issue |
| Hardware | 51 | Diagnose-and-replace workflow |
| Software | 49 | Licence issues, crashes, installation |
| Account Access | 45 | Password resets, MFA, lockouts |
| Email | 38 | Configuration, delivery, spam |
| Onboarding | 32 | Full new-hire IT setup procedure |
| Security | 23 | Incident triage and escalation |

## 📁 Repository Structure

```
it-helpdesk-simulation/
├── data/
│   └── helpdesk_tickets.csv       # 320 simulated tickets with full metadata
├── dashboard/
│   └── helpdesk_dashboard.xlsx    # KPI dashboard — 3 sheets, pivot tables, charts
├── sop/
│   ├── password-reset-sop.md      # SOP-001: Password reset & account unlock
│   ├── new-employee-onboarding-sop.md  # SOP-002: Full onboarding procedure
│   ├── vpn-troubleshooting-sop.md  # SOP-004: VPN diagnostic tree
│   └── README.md                  # SOP index
├── docs/
│   └── escalation-matrix.md       # Full escalation paths by issue type
└── build_helpdesk_project.py      # Python script that generated ticket data
```

## 🗂️ Dashboard Contents

**Sheet 1 — KPI Dashboard:**
- 5 KPI summary cards (total tickets, FCR, SLA, CSAT, resolution rate)
- Tickets by category table with SLA and FCR breakdown
- Bar chart: ticket volume by category
- Priority distribution with SLA compliance per priority level

**Sheet 2 — Ticket Log:**
- Full 320-row ticket dataset with all fields
- Filterable by date, category, priority, agent, status

**Sheet 3 — Agent Performance:**
- Per-agent breakdown of tickets, SLA compliance, FCR rate, and CSAT

## 📄 SOP Highlights

**SOP-001: Password Reset** — Identity verification protocol, Active Directory steps, MFA reset, notification template, escalation matrix, common errors table

**SOP-002: New Employee Onboarding** — Day -5 to Day +5 timeline, account creation checklist, hardware setup, Day 1 walkthrough script, asset tracking

**SOP-004: VPN Troubleshooting** — 6-step diagnostic tree (single vs multi-user), credential/MFA checks, client reinstall procedure, error code reference table

## 🔗 Connect
**Ernestina Thembi Zah** · [LinkedIn](https://linkedin.com/in/zahthembiernestina) · tinathembizah@gmail.com · Open to remote IT Support roles
