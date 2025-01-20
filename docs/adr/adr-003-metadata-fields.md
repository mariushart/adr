# Metadata Fields Definition

## Metadata
- ID: ADR-003
- Type: ADR
- Status: Accepted
- Date: 2025-01-20
- Deciders: mariushart

## Relationships
### Dependencies
- Requires: ADR-002 (Template Structure)
- Influences: All future ADRs

### Impact Analysis
- Strength: High
- Scope: Documentation Standards, Searchability
- Reversibility: Medium
- Technical Debt: Low

## Context
Proper metadata is crucial for organizing, tracking, and maintaining ADRs over time. We need to define a comprehensive set of metadata fields that provide quick insight into an ADR's purpose, status, and relationships while supporting future automation and tooling.

## Decision Story
- In the context of: establishing ADR metadata standards
- Facing concern(s):
  - Need for consistent categorization
  - Support for future automation
  - Balance between information and overhead
  - Version control and status tracking
- We decided: to implement a structured metadata section with specific required fields
- And not:
  - Use free-form tags
  - Rely solely on file naming
  - Include all possible fields
- To achieve:
  - Clear categorization and status tracking
  - Support for tooling and automation
  - Easy filtering and searching
- Accepting:
  - Maintenance overhead for metadata
  - Need to validate field consistency
  - Some fields may not apply to all ADRs

## Decision
We will implement the following metadata fields:
1. ID: Sequential number with prefix (e.g., ADR-001)
2. Type: Category of decision (ADR, RFC, etc.)
3. Status: One of [Proposed, Accepted, Deprecated, Superseded]
4. Date: ISO format (YYYY-MM-DD)
5. Deciders: List of decision-makers and their roles

## Rationale
- Chosen because:
  - Provides essential categorization
  - Supports version control and tracking
  - Enables automated processing
  - Balances completeness with usability
- Alternatives considered:
  - Minimal metadata: Insufficient for tracking
  - Extended metadata: Too much overhead
  - Free-form metadata: Hard to process automatically

## Consequences
- Positive:
  - Consistent categorization
  - Easy filtering and searching
  - Clear decision tracking
  - Support for automation
- Negative:
  - Additional maintenance requirements
  - Need for metadata validation
  - Potential for inconsistency
- Risks:
  - Incomplete metadata entry
  - Inconsistent status updates
  - Metadata drift over time

## Technical Details
- Field Formats:
  - ID: ADR-NNN format
  - Type: Enumerated values
  - Status: Enumerated values
  - Date: ISO 8601 (YYYY-MM-DD)
  - Deciders: Comma-separated list with roles
- Validation Rules:
  - All fields required
  - ID must be unique
  - Status must be from defined list
  - Date must be valid ISO format

## References
- Standards: ISO 8601 Date Format
- Patterns: Metadata in Documentation
- Documentation: Validation Scripts