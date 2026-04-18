# AI Evaluation Examples

This document demonstrates how AI-generated scenarios are evaluated for reasoning quality, completeness, and execution feasibility.

---

## Example 1: Incomplete Scenario

### Input Scenario
Task: "Book a flight tomorrow"

### Issues Identified
- Missing source and destination
- No time constraints
- No budget or preference criteria
- Ambiguous execution requirements

### Evaluation

| Criteria | Assessment |
|--------|------------|
| Logical Consistency | Partial – task is valid but underspecified |
| Context Completeness | Poor – missing critical inputs |
| Execution Feasibility | Low – cannot be executed reliably |

---

## Improved Scenario

### Refined Task
"Book a flight from New York (JFK) to San Francisco (SFO) tomorrow between 8AM–12PM under $500, preferring non-stop flights."

### Improvements
- Defined origin and destination
- Added time window
- Introduced budget constraint
- Included preference criteria

### Evaluation

| Criteria | Assessment |
|--------|------------|
| Logical Consistency | High |
| Context Completeness | High |
| Execution Feasibility | High |

---

## Example 2: AI Hallucination Case

### AI Output
"Flights under $200 are available tomorrow for all routes."

### Issues Identified
- Unrealistic generalization
- No data source or validation
- Assumes universal availability

### Hallucination Type
- Factual hallucination
- Logical overgeneralization

### Corrective Feedback
- Require data source validation
- Introduce constraints (route, airline, timing)
- Avoid universal claims

---

## Example 3: Multi-Agent Workflow Evaluation

### Workflow
Trend Discovery → Content Generation → Image Creation → Scheduling

### Issues Identified
- Missing feedback loop between generation and validation
- No error handling between agents
- Lack of performance metrics

### Recommendation
- Introduce validation agent before scheduling
- Add retry/error handling logic
- Define KPIs for output quality

---

## Summary

This evaluation approach focuses on:
- Reasoning correctness
- Context completeness
- Execution feasibility
- Hallucination detection

The goal is to ensure AI outputs are **usable, reliable, and production-ready**, not just syntactically correct.

## JSON Validation Example

Input:
{
  "task": "book flight",
  "date": "tomorrow"
}

Issues:
- Missing origin/destination
- No constraints
- Ambiguous execution

Improved:
{
  "task": "book flight",
  "from": "NYC",
  "to": "SFO",
  "date": "2026-04-20",
  "time_window": "8AM-12PM",
  "budget": 500
}
