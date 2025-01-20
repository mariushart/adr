# ADR Versioning Strategy

## Metadata
- ID: ADR-005
- Type: ADR
- Status: Proposed
- Date: 2025-01-20
- Deciders: Repository Maintainers

## Relationships
### Dependencies
- Requires: ADR-001 (Need for ADR)
- Influences: ADR-003 (Metadata Fields)

### Impact Analysis
- Strength: Medium
- Scope: Version Control, Change Management
- Reversibility: Medium
- Technical Debt: Low

## Context
ADRs document architectural decisions that evolve with the system. We need to determine how to version these documents in relation to the software repository's semantic versioning. While aligning ADR versions with the repository version might seem intuitive, we need to consider the distinct lifecycle of architectural decisions.

## Decision Story
- In the context of: managing ADR versions over time
- Facing concern(s):
  - Need to track ADR evolution
  - Relationship between code and architectural decisions
  - Handling superseded decisions
  - Managing backwards compatibility
- We decided: to maintain ADRs as immutable records with status changes
- And not:
  - Version ADRs independently
  - Directly tie ADRs to repository versions
  - Update existing ADRs in place
- To achieve:
  - Clear historical record
  - Simple version management
  - Easy traceability
- Accepting:
  - Need for explicit superseding ADRs
  - Potential disconnect from code versions
  - Additional status management overhead

## Decision
We will implement the following versioning strategy:

1. ADRs will be treated as immutable records
2. Changes to architectural decisions will be documented as new ADRs that supersede previous ones
3. The status field will be used to track the lifecycle:
   - PROPOSED -> ACCEPTED -> DEPRECATED/SUPERSEDED
4. Each ADR will reference the repository version range where it was active
5. The README will maintain a compatibility matrix:
   ```markdown
   | ADR ID | Title | Status | Valid From Version | Valid To Version |
   |--------|-------|--------|-------------------|------------------|
   | ADR-001| ...   | Active | 1.0.0            | current          |
   | ADR-002| ...   | Super. | 1.0.0            | 2.0.0           |
   ```

## Rationale
- Chosen because:
  - Preserves decision history
  - Simplifies version management
  - Makes changes explicit
  - Maintains clear traceability
- Alternatives considered:
  - Independent versioning: Too complex to manage
  - Direct repo version alignment: Masks decision evolution
  - In-place updates: Loses historical context

## Consequences
- Positive:
  - Clear decision history
  - Simple versioning model
  - Explicit change tracking
  - Easy to understand current state
- Negative:
  - More ADRs over time
  - Need to maintain compatibility matrix
  - Additional cross-referencing
- Risks:
  - Matrix maintenance overhead
  - Potential confusion about active decisions
  - Version range gaps

## Technical Details
- Status Transitions:
  - PROPOSED -> ACCEPTED: When implementation begins
  - ACCEPTED -> DEPRECATED: When decision is no longer valid
  - ACCEPTED -> SUPERSEDED: When replaced by new ADR
- Version Range Format:
  - Use semantic versioning (MAJOR.MINOR.PATCH)
  - "current" keyword for active decisions
- Matrix Management:
  - Maintained in repository README
  - Updated with each ADR status change
  - Validated by CI/CD pipeline

## References
- Standards: Semantic Versioning 2.0.0
- Patterns: Immutable Records
- Documentation: Version Control Best Practices