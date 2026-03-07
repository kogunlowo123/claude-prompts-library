# Security Audit Prompt

## Purpose

Conduct systematic security assessments of applications, infrastructure, and configurations.

## System Prompt

```
You are a senior security engineer conducting a thorough security audit. You follow OWASP guidelines, CIS benchmarks, and industry best practices. You prioritize findings by risk level and provide actionable remediation steps.
```

## Prompt Template

```
Perform a security audit of the following:

**Audit Target:** {target}  (application / infrastructure / configuration)
**Technology Stack:** {stack}
**Compliance Requirements:** {compliance}  (SOC2 / HIPAA / PCI-DSS / GDPR / none)

**Materials to Review:**
{materials}

Assess the following areas:
1. **Authentication & Authorization**: Password policies, MFA, session management, RBAC
2. **Data Protection**: Encryption at rest and in transit, key management, data classification
3. **Input Validation**: Injection prevention, file upload handling, API input sanitization
4. **Infrastructure Security**: Network segmentation, firewall rules, patch management
5. **Logging & Monitoring**: Audit trails, alerting, incident detection
6. **Dependency Security**: Known vulnerabilities, supply chain risks, update policies
7. **Configuration**: Secure defaults, hardening, secrets management

For each finding:
- Severity: CRITICAL / HIGH / MEDIUM / LOW / INFORMATIONAL
- Category: (from the areas above)
- Description: What the issue is
- Risk: Potential impact if exploited
- Remediation: Specific steps to fix
- Priority: Immediate / Short-term / Long-term
```

## Focused Audits

### API Security
```
Audit this API for security vulnerabilities:
{api_spec}

Focus on: authentication, rate limiting, input validation,
error information disclosure, CORS configuration.
```

### Container Security
```
Audit this Dockerfile and container configuration:
{dockerfile}

Check: base image vulnerabilities, running as root, exposed secrets,
unnecessary packages, health checks, resource limits.
```

### Cloud Configuration
```
Audit this cloud infrastructure configuration:
{config}

Check: IAM policies, public exposure, encryption settings,
logging configuration, network ACLs, backup policies.
```
