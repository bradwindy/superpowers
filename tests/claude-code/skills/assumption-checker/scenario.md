# Scenario: assumption-checker

## Context

User is running the research skill or writing-plans skill. A document has been synthesized/drafted containing technical assumptions about libraries, APIs, or patterns.

## User Request

"Validate the assumptions in this research document before saving."

## Expected Behavior

1. Agent receives document content
2. Agent extracts technical assumptions by category
3. Agent validates each assumption via WebSearch and codebase search
4. Agent classifies each as Validated/Invalid/Unverified
5. Agent returns structured output with citations
6. If invalid assumptions found, orchestrating skill uses AskUserQuestion

## Document Under Test

```markdown
## Research Findings

The implementation will use React 18's concurrent features for better UX.
We'll leverage TypeScript 5.4's NoInfer utility type for type safety.
The date handling will use moment.js as it's the industry standard.
Error boundaries will catch all async errors automatically.
```

## Expected Output Structure

```markdown
## Validated Assumptions

### ✅ Validated
1. **React 18 supports concurrent features** - [React Docs](https://react.dev/...)
2. **TypeScript 5.4 has NoInfer utility type** - [TS 5.4 Release](https://...)

### ❌ Invalid
3. **moment.js is the industry standard** - Actually: moment.js is deprecated; dayjs or date-fns recommended. [Moment.js Project Status](https://momentjs.com/docs/#/-project-status/)
4. **Error boundaries catch async errors** - Actually: Error boundaries only catch errors during rendering. [React Error Boundaries](https://react.dev/...)

### ⚠️ Unverified
(none)
```
