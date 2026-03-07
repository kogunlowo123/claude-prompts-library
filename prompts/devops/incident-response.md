# Incident Response Prompt

## Purpose

Guide structured incident response from detection through resolution and post-mortem.

## System Prompt

```
You are a senior SRE leading incident response. You prioritize restoring service, communicate clearly, and follow structured incident management processes. You think systematically about blast radius, dependencies, and rollback options.
```

## Prompt Template

```
Help me respond to this production incident.

**Incident Summary:**
{summary}

**Severity:** {severity}  (SEV1 / SEV2 / SEV3 / SEV4)
**Affected Services:** {services}
**Impact:** {impact}  (user-facing / internal / data integrity)
**Start Time:** {start_time}
**Current Status:** {status}

**Symptoms/Alerts:**
{symptoms}

**Recent Changes:**
{changes}

**Available Data:**
{data}

Please provide:
1. **Immediate Actions**: Steps to mitigate impact right now
2. **Diagnosis Plan**: Systematic approach to identify root cause
3. **Communication Template**: Stakeholder update message
4. **Rollback Assessment**: Can we roll back recent changes?
5. **Escalation Criteria**: When to escalate and to whom
6. **Resolution Steps**: Once root cause is identified
7. **Post-Incident Tasks**: What to document and follow up on
```

## Communication Templates

### Status Update
```
**Incident Update - {timestamp}**
Status: {investigating/identified/monitoring/resolved}
Impact: {impact_description}
Current action: {what_team_is_doing}
Next update: {eta}
```

### Post-Mortem Outline
```
1. Incident Timeline
2. Root Cause Analysis
3. Impact Assessment
4. What Went Well
5. What Could Be Improved
6. Action Items (with owners and deadlines)
```
