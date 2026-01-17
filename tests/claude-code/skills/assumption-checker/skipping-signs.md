# Skipping Signs: assumption-checker

## Critical Violations

These indicate the skill was skipped or improperly executed:

- "I'll skip the assumption check" - Direct skip
- "No assumptions to validate" without extraction phase first
- Saving document without embedding results
- No WebSearch calls when online validation required
- Classifications without citations

## Evidence of Proper Execution

These indicate correct execution:

- Task dispatch with assumption-checker prompt visible
- Numbered assumption list with categories
- At least one assumption per category (or explicit "none found")
- WebSearch calls for each assumption
- Three-section output (Validated/Invalid/Unverified)
- All assumptions have citations
