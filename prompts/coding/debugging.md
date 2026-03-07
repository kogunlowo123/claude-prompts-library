# Debugging Prompt

## Purpose

Systematically diagnose and resolve software bugs using structured analysis.

## System Prompt

```
You are an expert software debugger. You approach problems methodically, forming hypotheses and testing them systematically. You consider the full stack and common failure patterns for the given technology.
```

## Prompt Template

```
I need help debugging an issue. Please analyze systematically.

**Environment:**
- Language/Runtime: {language} {version}
- Framework: {framework}
- OS: {os}
- Relevant dependencies: {dependencies}

**Expected Behavior:**
{expected}

**Actual Behavior:**
{actual}

**Error Message/Stack Trace:**
```
{error}
```

**Steps to Reproduce:**
{steps}

**What I've Already Tried:**
{attempted_fixes}

**Relevant Code:**
```{language}
{code}
```

Please:
1. Analyze the error message and stack trace
2. Form hypotheses about the root cause (list top 3)
3. For each hypothesis, suggest a diagnostic step
4. Provide the most likely fix with code
5. Suggest preventive measures to avoid this class of bug
```

## Variations

### Quick Debug
```
Debug this error in {language}:
Error: {error}
Code: {code}
What's wrong and how do I fix it?
```

### Performance Debug
```
This code is running slower than expected. Profile data shows:
{profile_data}

Code:
{code}

Identify the bottleneck and suggest optimizations.
```

### Intermittent Bug
```
This bug occurs intermittently (~20% of requests). It works fine most of the time.

Error when it fails: {error}
Code: {code}

What race conditions, timing issues, or external dependencies could cause this?
```
