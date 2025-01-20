# Template Structure Design

## Metadata
- ID: ADR-002
- Type: ADR
- Status: Accepted
- Date: 2025-01-20
- Deciders: mariushart

## Relationships
### Dependencies
- Requires: ADR-001 (Need for ADR)
- Enables: ADR-003 (Metadata Fields), ADR-004 (Impact Analysis)

### Impact Analysis
- Strength: High
- Scope: Documentation Format, User Experience
- Reversibility: Medium
- Technical Debt: Low

## Context
After establishing the need for ADRs, we must define a clear, consistent structure that balances comprehensiveness with usability. The template structure needs to guide users through documenting their architectural decisions while remaining flexible enough for different types of decisions.

## Decision Story
- In the context of: creating a standardized ADR format
- Facing concern(s):
  - Need for consistent documentation structure
  - Balance between completeness and usability
  - Supporting different decision types
  - Ensuring key information is captured
- We decided: to implement a structured template with distinct sections for context, decision story, rationale, and consequences
- And not:
  - Use a free-form format
  - Use a structured data format
  - Create separate templates for each decision type
  - Implement a minimal template
- To achieve:
  - Consistent documentation across projects
  - Complete capture of decision context and reasoning
  - Easy navigation and understanding
- Accepting:
  - Some sections may not apply to all decisions
  - Initial learning curve for new users
  - Need for documentation about the template itself
  - Not readily machine-readable format

## Decision
We will implement a template with the following major sections:
1. Metadata: For quick reference and categorization
2. Relationships: To track dependencies and impacts
3. Context: To explain the background and drivers
4. Decision Story: To capture the narrative and reasoning
5. Decision: To clearly state the outcome
6. Rationale: To document the "why"
7. Consequences: To record impacts and trade-offs
8. Technical Details: Optional section for implementation specifics
9. References: For related documentation and standards

## Rationale
- Chosen because:
  - Provides clear structure for decision documentation
  - Captures both technical and contextual information
  - Supports future understanding and review
  - Balances detail with usability
- Alternatives considered:
  - Lightweight format: Too little context captured
  - Multiple specialized templates: Too complex to maintain
  - Problem-solution format: Too simplistic for architectural decisions

## Consequences
- Positive:
  - Consistent documentation format
  - Complete capture of decision context
  - Clear separation of concerns
  - Supports future decision review
- Negative:
  - More extensive than some users might prefer
  - Requires initial training/familiarization
  - May seem formal for smaller decisions
- Risks:
  - Template might be seen as too rigid
  - Some sections might be left empty
  - Possible resistance to formal structure

## Technical Details
- Format: Markdown
- Section Order: Designed for logical flow of information
- Required vs Optional Sections:
  - Required: Metadata, Context, Decision, Consequences
  - Optional: Technical Details, References
- Formatting Requirements:
  - Use of headers for sections (H1 for title, H2 for sections)
  - Consistent bullet points for lists
  - Code blocks for technical content

## References
- Standards: Markdown Guide
- Patterns: Documentation as Code
- Documentation: Template Usage Guide