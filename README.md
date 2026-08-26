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
