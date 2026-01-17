# Checklist: assumption-checker Compliance

## Extraction Gate (COMPULSORY)
- [ ] Document content received by agent
- [ ] Assumptions extracted from input document
- [ ] Each assumption categorized (library/API/pattern/performance/security)
- [ ] Assumptions numbered for tracking
- [ ] At least one assumption per category OR explicit "none found"

## Validation Gate (COMPULSORY)
- [ ] Each assumption has validation status (✅/❌/⚠️)
- [ ] Each validation has source citation (URL or file:line)
- [ ] Invalid assumptions include correction text
- [ ] WebSearch used for online validation
- [ ] Grep/Glob used for codebase pattern check

## Output Gate (COMPULSORY)
- [ ] Structured output with three sections (Validated/Invalid/Unverified)
- [ ] All assumptions accounted for in output
- [ ] Citations present for each classification
- [ ] Error states handled gracefully (timeout, empty doc, conflicts)

## Evidence Requirements
- [ ] Task dispatch with assumption-checker prompt visible
- [ ] At least one assumption extracted
- [ ] At least one WebSearch call made
- [ ] Structured markdown output returned
