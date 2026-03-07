# Runbook Generation Prompt

## Purpose

Create operational runbooks for common procedures, maintenance tasks, and emergency operations.

## System Prompt

```
You are a senior operations engineer who writes clear, tested runbooks. Your runbooks are step-by-step, include verification at each stage, have rollback procedures, and are written so that an on-call engineer at 3 AM can follow them successfully.
```

## Prompt Template

```
Create an operational runbook for: {operation}

**System:** {system}
**Environment:** {environment}  (production / staging / development)
**Frequency:** {frequency}  (ad-hoc / daily / weekly / quarterly)
**Risk Level:** {risk}  (low / medium / high / critical)

**Prerequisites:**
{prerequisites}

Please include:
1. **Overview**: What this runbook does and when to use it
2. **Prerequisites Checklist**: Access, tools, approvals needed
3. **Pre-Flight Checks**: Validations before starting
4. **Step-by-Step Procedure**: Numbered steps with expected output
5. **Verification**: How to confirm each step succeeded
6. **Rollback Procedure**: How to undo changes if something goes wrong
7. **Post-Completion Checks**: Final validation steps
8. **Troubleshooting**: Common issues and their resolutions
9. **Contacts**: Who to escalate to if stuck

Format each step as:
### Step N: {description}
**Command:**
```bash
{command}
```
**Expected Output:** {output}
**If it fails:** {failure_action}
```

## Variations

### Database Migration Runbook
```
Create a runbook for running database migrations in production.
Database: {database_type}
Migration tool: {tool}
Include: backup procedure, migration execution, validation queries, rollback steps.
```

### Deployment Runbook
```
Create a deployment runbook for: {service}
Deployment method: {method}
Include: pre-deployment checks, deployment steps, smoke tests, rollback procedure.
```

### Disaster Recovery Runbook
```
Create a DR runbook for: {system}
RPO: {rpo}
RTO: {rto}
Include: failover procedure, data recovery, DNS changes, validation, failback.
```
