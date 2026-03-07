# Few-Shot Prompt Template

## Purpose

A template for constructing effective few-shot prompts that guide model behavior through examples.

## Template Structure

```
{task_description}

Here are some examples:

**Example 1:**
Input: {input_1}
Output: {output_1}

**Example 2:**
Input: {input_2}
Output: {output_2}

**Example 3:**
Input: {input_3}
Output: {output_3}

Now process the following:
Input: {actual_input}
Output:
```

## Best Practices

### Example Selection
- Choose examples that cover different edge cases
- Include at least one "typical" case and one "tricky" case
- Order examples from simple to complex
- Use 3-5 examples for most tasks (more for complex formats)

### Example Quality
- Ensure all examples are correct and consistent
- Use the exact output format you want in every example
- Make examples representative of real inputs
- Avoid ambiguous cases in examples

### Diversity
- Cover different categories or classes
- Include boundary cases
- Vary input length and complexity
- Represent different formatting scenarios

## Examples by Task Type

### Classification
```
Classify the following support tickets by category.

Ticket: "My password reset email never arrived"
Category: Authentication

Ticket: "The dashboard loads slowly on mobile"
Category: Performance

Ticket: "I was charged twice for my subscription"
Category: Billing

Ticket: "{new_ticket}"
Category:
```

### Extraction
```
Extract structured data from the following job postings.

Posting: "Senior Python Developer at TechCorp, NYC. 5+ years experience. $150k-180k."
Result: {"title": "Senior Python Developer", "company": "TechCorp", "location": "NYC", "experience": "5+ years", "salary": "$150k-$180k"}

Posting: "Remote DevOps Engineer, StartupXYZ. 3 years minimum. Competitive salary."
Result: {"title": "DevOps Engineer", "company": "StartupXYZ", "location": "Remote", "experience": "3+ years", "salary": "Not specified"}

Posting: "{new_posting}"
Result:
```

### Transformation
```
Convert the following natural language queries to SQL.

Query: "Show me all users who signed up last month"
SQL: SELECT * FROM users WHERE created_at >= DATE_TRUNC('month', CURRENT_DATE - INTERVAL '1 month') AND created_at < DATE_TRUNC('month', CURRENT_DATE);

Query: "Count orders by status"
SQL: SELECT status, COUNT(*) as order_count FROM orders GROUP BY status ORDER BY order_count DESC;

Query: "{new_query}"
SQL:
```

## Anti-Patterns to Avoid

- Using too many examples (cognitive overload)
- Inconsistent formatting between examples
- Examples that contradict each other
- Overly simple examples that do not teach the pattern
- Missing edge cases that appear in real inputs
