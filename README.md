# Architecture Decision Records (ADR) Framework
Version 0.1

A comprehensive framework for creating, managing, and analyzing Architecture Decision Records (ADRs) across projects and enterprises.

## Table of Contents
- [Overview](#overview)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
- [Framework Features](#framework-features)
- [Usage Guidelines](#usage-guidelines)
- [Tools](#tools)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

This repository provides a standardized approach to documenting architectural decisions through ADRs. It includes templates, examples, and tools that support both individual project decisions and enterprise-wide architectural governance.

## ADR log

| ADR ID | Title | Status | Valid From Version | Valid To Version |
|--------|-------|--------|-------------------|------------------|
| ADR-001| Need for ADR  | Accepted | 1.0.0            | current          |
| ADR-002| Template structure   | Accepted | 1.0.0            | current       |
| ADR-003| Metadata fields  | Accepted | 1.0.0            | current       |
| ADR-004| Impact analysis  | Accepted | 1.0.0            | current       |
| ADR-005| ADR versioning   | Accepted | 1.0.0            | current       |
| ADR-006| Enterprise wide   | Accepted | 1.0.0            | current       |
| ADR-007| Automated enterprise monitoring | Proposed | 1.0.0            | current       |


## Repository Structure

```
.
├── docs/
│   ├── adr/                  # Framework ADRs
│   │   ├── adr-001-need-for-adr.md
│   │   ├── adr-002-template-structure.md
│   │   ├── adr-003-metadata-fields.md
│   │   ├── adr-004-impact-analysis-framework.md
│   │   ├── adr-005-adr-versioning-strategy.md
│   │   ├── adr-006-enterprise-wide-adr-management.md
│   │   └── adr-007-automated-ea-monitoring-of-adrs.md
│   └── glossary.md          # Terminology and concepts
├── examples/
│   └── adr_example.md       # Example ADRs
├── templates/
│   └── full.md              # ADR templates
├── tools/
│   └── validators/          # Validation tools TODO
├── LICENSE
└── README.md
```

## Getting Started

1. **New to ADRs?**
   - Read [ADR-001](docs/adr/adr-001-need-for-adr.md) for background
   - Review the [example ADR](examples/adr_example.md)
   - Check the [glossary](docs/glossary.md) for terminology

2. **Creating ADRs**
   - Copy [full template](templates/full.md) to your project
   - Follow the template structure
   - Use consistent naming: `adr-NNN-title.md`

3. **Project Integration**
   ```bash
   # Create ADR directory in your project
   mkdir -p docs/adr
   
   # Copy template and tools
   cp templates/full.md docs/adr/adr-template.md
   cp -r tools/validators .
   ```

## Framework Features

- **Standardized Format**: Consistent, machine-readable ADR structure
- **Enterprise Support**: Tools and formats for EA oversight
- **Version Control**: Clear strategy for managing ADR lifecycles
- **Impact Analysis**: Framework for assessing architectural impacts
- **Automation Ready**: Support for automated monitoring and analysis

## Usage Guidelines

### Individual Projects
1. Place ADRs in `docs/adr/` directory
2. Use sequential numbering: `adr-NNN-title.md`
3. Follow the template structure
4. Maintain ADR status updates

### Enterprise Architecture
1. Monitor ADRs across repositories
2. Analyze architectural patterns
3. Track technology decisions
4. Assess cross-cutting concerns

## Tools

### Validators TODO
- Format validation
- Cross-reference checking
- Status consistency
- Relationship validation

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Open a pull request

## License

MIT License

Copyright (c) 2025 

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
