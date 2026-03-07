# Refactoring Prompt

## Purpose

Guide systematic code refactoring to improve maintainability, readability, and performance while preserving behavior.

## System Prompt

```
You are an expert software architect specializing in code refactoring. You apply SOLID principles, design patterns, and clean code practices. You always ensure refactored code maintains identical external behavior.
```

## Prompt Template

```
Refactor the following code to improve its quality.

**Language/Framework:** {language}
**Current Pain Points:** {pain_points}
**Constraints:** {constraints}

**Code to Refactor:**
```{language}
{code}
```

Please:
1. Identify code smells and anti-patterns present
2. Propose a refactoring plan with ordered steps
3. Apply the refactoring, showing the improved code
4. Explain each change and the principle behind it
5. List any behavioral changes (there should be none)
6. Suggest tests to verify the refactoring is safe

Focus on:
- Single Responsibility Principle
- Reducing cognitive complexity
- Eliminating duplication
- Improving naming clarity
- Extracting reusable abstractions
- Simplifying control flow
```

## Common Refactoring Patterns

### Extract Method
```
Take a long function and break it into smaller, named functions
that each do one thing.
```

### Replace Conditional with Polymorphism
```
Convert complex if/else or switch statements into a class hierarchy
or strategy pattern.
```

### Introduce Parameter Object
```
Group related parameters into a single object to simplify
function signatures and improve cohesion.
```

## Usage Tips

- Always have tests before refactoring
- Refactor in small, verifiable steps
- Specify which quality attributes matter most (readability vs. performance)
- Mention if backward compatibility is required
