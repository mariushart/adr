# [Title]

## Metadata
- ID: [number]
- Type: ADR
- Status: [Proposed | Accepted | Deprecated | Superseded]
- Date: [YYYY-MM-DD]
- Deciders: [list of decision-makers]

## Relationships
### Dependencies
- Requires: [ADR][Description] fx ADR-038 (Message Broker) - Hard dependency for event distribution
- Enables: [ADR][Description] fx ADR-045 (Database Choice) - Influences available technology options
- Supersedes: [ADR][Description] fx ADR-028 (Old Data Approach) - Replaces previous consistency model

### Impact Analysis
- Strength: [None | Low | Medium | High] fx High
- Scope: Data Storage, API Design, Scalability
- Reversibility: [None | Low | Medium | High] fx Low
- Technical Debt: [None | Low | Medium | High] Medium

## Context
[Concise description of the forces driving this decision]

## Decision
<!-- P0483 -->
- In the context of: [Describe the context or background]
- Facing concern(s): [List the concerns or issues]
- We decided: [State the decision]
- And not: [Explain alternatives not chosen]
- To achieve: [Describe desired outcomes]
- Accepting: [List trade-offs/compromises]

## Rationale
- Chosen because:
  - [Key reasons]
- Alternatives considered:
  - [Alternative]: [Why not chosen]

## Consequences
- Positive: [list]
- Negative: [list]
- Risks: [list]

## Technical Details
[Optional section for technical ADRs]
- Implementation requirements
- Class/component diagrams
- API definitions

## References
- Standards: [links to relevant standards]
- Patterns: [links to pattern catalog]
- Documentation: [links to docs]
