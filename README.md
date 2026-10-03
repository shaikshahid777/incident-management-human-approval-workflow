<!-- SHOWCASE_START --><div align="center">[![Typing](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=22&duration=2800&pause=900&color=58A6FF&center=true&vCenter=true&width=900&lines=incident%20management%20human%20approval%20workflow;AI%20%7C%20Automation%20%7C%20Engineering;Explore%20the%20project%20%F0%9F%9A%80)](https://github.com/shaikshahid777/incident-management-human-approval-workflow)<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:161B22,100:58A6FF&height=110&section=header&text=incident-management-human-approval-workflow&fontSize=26&fontColor=FFFFFF&animation=twinkling&fontAlignY=65" width="100%" alt="Animated project banner"/>

[![Repository](https://img.shields.io/badge/Repository-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/shaikshahid777/incident-management-human-approval-workflow) [![Issues](https://img.shields.io/badge/Report-Issue-red?style=for-the-badge&logo=github)](https://github.com/shaikshahid777/incident-management-human-approval-workflow/issues/new) [![Stars](https://img.shields.io/github/stars/shaikshahid777/incident-management-human-approval-workflow?style=for-the-badge&logo=github)](https://github.com/shaikshahid777/incident-management-human-approval-workflow/stargazers) [![Fork](https://img.shields.io/github/forks/shaikshahid777/incident-management-human-approval-workflow?style=for-the-badge&logo=github)](https://github.com/shaikshahid777/incident-management-human-approval-workflow/fork) [![Profile](https://img.shields.io/badge/Profile-Visit-0A66C2?style=for-the-badge&logo=github)](https://github.com/shaikshahid777)</div>

> ✨ **Project Showcase Mode:** animated banner • interactive navigation • live repository actions

[🚀 Repository](https://github.com/shaikshahid777/incident-management-human-approval-workflow) · [🐞 Report Issue](https://github.com/shaikshahid777/incident-management-human-approval-workflow/issues/new) · [⭐ Star](https://github.com/shaikshahid777/incident-management-human-approval-workflow/stargazers) · [🔱 Fork](https://github.com/shaikshahid777/incident-management-human-approval-workflow/fork) · [👤 Profile](https://github.com/shaikshahid777)

<!-- SHOWCASE_END -->

# Incident Management & Human Approval Workflow

Lesson 5 n8n assessment covering incident intake, duplicate-alert throttling, severity routing, notification, SLA escalation, human approval, webhook-based resumption, and Approved/Rejected decision paths.

## Assessment Scope

- Incident trigger using Manual Trigger or Webhook
- Alert throttling and duplicate suppression
- CRITICAL / INFO / fallback severity routing
- Slack incident notification
- SLA wait: 10 minutes in production; 30 seconds during testing if needed
- Twilio SMS escalation for unacknowledged incidents
- Interactive human approval with Approve / Reject decisions
- POST webhook callback at `slack-approval-response`
- Approved and Rejected processing paths
- Production-style naming and annotations

## Workflow Structure

```text
Incident Trigger
      ↓
Alert Throttle Check
      ↓
Is Alert Eligible?
   ↙            ↘
Route by Severity   Suppress Duplicate Alert
   ↓
CRITICAL / INFO / Other
   ↓
Acknowledgement / Approval / Decision Paths
```

## Important Testing Note

Slack and Twilio live delivery require valid credentials. During development, notification/approval branches may be prepared using test configurations, but any such limitation should be stated clearly in the LMS submission and documentation.

## Security

Do not commit Slack tokens, Twilio credentials, webhook secrets, passwords, or other sensitive credentials to this public repository. Keep credentials in n8n Credential Manager.

## Submission Files

Recommended repository structure:

```text
incident-management-human-approval-workflow/
├── README.md
├── workflow/
│   └── Incident_Management_Human_Approval.json
├── documentation/
│   └── Incident_Management_Human_Approval_Workflow_Documentation.pdf
├── screenshots/
└── evidence/
```

## Loom

https://www.loom.com/share/454969b32c5449c78cae4a74d622d020
