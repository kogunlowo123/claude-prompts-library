# Code Review Prompt

## Purpose

Perform thorough code reviews identifying bugs, security issues, performance problems, and style inconsistencies.

## System Prompt

```
You are an expert code reviewer with deep knowledge of software engineering best practices, security vulnerabilities, and performance optimization. Review code thoroughly and provide actionable feedback.
```

## Prompt Template

```
Review the following code and provide feedback on:

1. **Bugs and Logic Errors**: Identify any incorrect logic, off-by-one errors, null/undefined handling, race conditions, or edge cases
2. **Security Vulnerabilities**: Check for injection attacks, authentication issues, data exposure, insecure defaults
3. **Performance**: Identify N+1 queries, unnecessary allocations, missing indexes, inefficient algorithms
4. **Code Quality**: Assess naming conventions, function length, single responsibility, DRY violations
5. **Error Handling**: Evaluate try/catch usage, error propagation, user-facing error messages
6. **Testing**: Note any untestable code patterns or missing test scenarios

**Language/Framework:** {language}
**Context:** {context}

**Code to Review:**
```{language}
{code}
```

For each finding, provide:
- Severity: CRITICAL / HIGH / MEDIUM / LOW
- Line reference
- Description of the issue
- Suggested fix with code example
```

## Usage Tips

- Provide context about the codebase and its purpose
- Specify the language and framework version
- Include related files if the review depends on external interfaces
- Mention any specific areas of concern

## Example Output Format

```
## Code Review Summary

### Critical Issues (0)
None found.

### High Severity (1)
1. **SQL Injection Vulnerability** (Line 23)
   - The query uses string interpolation instead of parameterized queries
   - Fix: Use prepared statements
   ```python
   cursor.execute("SELECT * FROM users WHERE id = %s", (user_id,))
   ```

### Medium Severity (2)
...
```
