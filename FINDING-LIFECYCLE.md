# FINDING-LIFECYCLE

```text
DISCOVER
   ↓
REPRODUCE
   ↓
MINIMIZE
   ↓
CLASSIFY
   ↓
EVIDENCE
   ↓
REVIEW
   ↓
ROUTE
   ↓
FIX
   ↓
REGRESSION
```

## 1. Discover

Record the initial observation without claiming a vulnerability.

## 2. Reproduce

Repeat the behavior under controlled conditions.

## 3. Minimize

Reduce the case to the smallest input, state and sequence that still reproduces it.

## 4. Classify

Separate observation, weakness, vulnerability, architectural failure, regression, false positive and unresolved state.

## 5. Evidence

Preserve logs, traces, versions, commits, screenshots, hashes and other artifacts needed for independent review.

## 6. Review

Check authorization, reproducibility, impact and alternative explanations.

## 7. Route

Select the affected component only after classification. Routing does not create ownership.

## 8. Fix

Apply a minimal change in the appropriate component.

## 9. Regression

Re-run the original test and add a regression case so the property remains protected.

## Closure rule

A finding is not closed because a change was made. It is closed only when the security property is re-tested and the result is recorded.
