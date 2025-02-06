# Enterprise Architecture Glossary

## Motivation Layer
### Strategy & Motivation
- **RCDA (Risk- and Cost-Driven Architecture)**
  - Architecting approach focusing on managing risks and costs in solution design
  - Key aspects:
    - Decision Stories
    - Risk-first approach
    - Cost optimization
    - Scalable methodology
    - Agile and deadline-oriented
    - Validated through peer-reviewed research
    - Recognized by Open Group Certified Architect (OpenCA) program
  - Related to: Decision Stories, Architecture Governance

- **Decision Stories**
  - Standardized method for documenting architectural choices
  - Structure:
    - In the context of: [situation/environment]
    - Facing concern(s): [problems/challenges]
    - We decided: [solution/approach]
    - And not: [rejected alternatives]
    - To achieve: [outcomes/benefits]
    - Accepting: [trade-offs/consequences]

- **RFC 2219**
  - Standard for unambiguous requirements specification
  - Key terms:
    - MUST/SHALL: Absolute requirement
    - MUST NOT/SHALL NOT: Absolute prohibition
    - SHOULD/RECOMMENDED: Valid exceptions possible with careful consideration
    - MAY/OPTIONAL: Truly optional items
  - Related to: Requirements Engineering

- **TOGAF**
  - Enterprise architecture methodology and framework
  - Architecture Development Method (ADM) components:
    - Preliminary: TOGAF implementation
    - Architecture Vision: Project scope and expectations
    - Business Architecture: Business structure and goals
    - Information Systems Architecture: Data and application
    - Technology Architecture: Infrastructure
    - Opportunities and Solutions: Implementation planning
    - Migration Planning: Cost-benefit and implementation
    - Implementation Governance: Architectural oversight
    - Architecture Change Management: Change monitoring

## Business Layer
### Process & Organization
- **Conway's Law**
  - Systems mirror organization's communication structure
  - Impact on: System architecture, Team boundaries, Integration patterns
  - Related to: Organization Design, System Architecture

- **Scaled Agile**
  - Merging of SCRUM/Agile with enterprise management
  - Antipatterns:
    - Ad hoc planning vs. architecture goals
    - Excessive non-technical meetings
    - Waterfall planning without analysis

- **SCRUM**
  - Framework for ~5 developers' self-organization
  - Success factor: Technical SCRUM master shielding team
  - Antipatterns: 
    - Micromanagement
    - Removal of self-organization
    - Focus on management tooling
    - Non-code-producing activities

- **Agile Manifesto**
  - Core values:
    - Individuals and interactions over processes and tools
    - Working software over comprehensive documentation
    - Customer collaboration over contract negotiation
    - Responding to change over following a plan

- **Project Blindness**
  - Consequences of individual project goals overshadowing enterprise benefits
  - Symptoms:
    - Local optimization
    - Duplicate functionality
    - Inconsistent technology choices
    - Fragmented architecture
    - Silos of knowledge
  - Root causes:
    - Project-based funding models
    - Short-term success metrics
    - Lack of enterprise architecture governance
    - Missing cross-project coordination
  - Related to: Technical Debt, Enterprise Architecture

- **Project-Product Mismatch**
  - Tension between project delivery and product maintenance
  - Manifestations:
    - Handover problems
    - Maintenance funding gaps
    - Missing long-term ownership
  - Related to: Project Blindness, Technical Debt

## Application Layer
### Architecture & Design
- **Architecture Decision Record (ADR)**
  - Documented record of significant architectural decisions
  - Components:
    - Context
    - Decision Story
    - Rationale
    - Consequences
    - Technical Details
  - Related to: Decision Log, Design Documentation

- **SOLID Principles**
  - Single Responsibility Principle (SRP)
    - Class should have one reason to change
    - Aspects:
      - Focused functionality
      - High cohesion
      - Clear boundaries
    - Related to: Separation of Concerns

  - Open/Closed Principle (OCP)
    - Open for extension, closed for modification
    - Implementation:
      - Interfaces and abstract classes
      - Plugin architecture
      - Behavior extension without modification
    - Related to: Interface-based Design

  - Liskov Substitution Principle (LSP)
    - Subtypes must be substitutable for base types
    - Key aspects:
      - Behavioral compatibility
      - Contract adherence
      - Type safety
    - Related to: Inheritance, Polymorphism

  - Interface Segregation Principle (ISP)
    - Clients shouldn't depend on unused interfaces
    - Key aspects:
      - Small, focused interfaces
      - Role-specific interfaces
      - Avoid fat interfaces
    - Related to: API Design

  - Dependency Inversion Principle (DIP)
    - High-level modules independent of low-level modules
    - Implementation:
      - Depend on abstractions
      - Inversion of Control (IoC)
      - Dependency Injection (DI)
    - Related to: Loose Coupling

- **Domain-Driven Design (DDD)**
  - Approach focusing on core domain
  - Key concepts:
    - Bounded Context: Specialized domain model
    - Ubiquitous Language: Common, precise terminology
    - Context Mapping: Documenting relationships
    - Aggregates: Consistency boundaries
    - Value Objects: Immutable domain concepts
  - Related to: Object-Oriented Design

- **Object-Oriented Analysis and Design (OOAD)**
  - Analysis (OOA):
    - Problem domain analysis
    - Objects and classes identification
    - Relationship mapping
    - Domain model creation
  - Design (OOD):
    - System structure design
    - Component interaction
    - Interface definition
    - Implementation patterns

### Development Practices
- **Code Smells**
  - Bloaters:
    - Long Method: Too many lines/responsibilities
    - Large Class: Too many fields/methods
    - Primitive Obsession: Overuse of primitives
    - Long Parameter List: Excessive parameters
    - Data Clumps: Repeating data groups

  - Change Preventers:
    - Divergent Change: Multiple reasons to modify
    - Shotgun Surgery: Changes scatter across codebase
    - Parallel Inheritance: Coupled hierarchies
    - Global State: Uncontrolled shared state
    - Message Chains: Excessive delegation

  - Couplers:
    - Feature Envy: Method uses another class's data
    - Inappropriate Intimacy: Classes too interconnected
    - Message Chains: Long method call sequences
    - Middle Man: Excessive delegation
    - Insider Trading: Hidden class communication

  - Object-Orientation Abusers:
    - Switch Statements: Type-based conditionals
    - Temporary Field: Context-dependent fields
    - Refused Bequest: Unused inheritance
    - Alternative Classes: Duplicate functionality

  - Dispensables:
    - Comments: Code-explaining comments
    - Duplicate Code: Repeated patterns
    - Lazy Class: Low-value components
    - Data Class: Behavior-less structure

- **Testing & Quality**
  - Test-Driven Development (TDD)
    - Write tests first
    - Red-Green-Refactor cycle
    - Design driver
  - Continuous Integration/Deployment
    - Automated builds
    - Test automation
    - Deployment pipeline
  - Code Review
    - Peer review process
    - Quality gates
    - Knowledge sharing

- **YAGNI (You Ain't Gonna Need It)**
  - Principle against premature functionality
  - Addresses: 
    - Overengineering
    - Unnecessary complexity
    - Speculative generality
  - Related to: Agile Development, Minimalism

## Technology Layer
### Infrastructure
- **Infrastructure as Code (IaC)**
  - Managing infrastructure through code
  - Types:
    - Declarative: Terraform, CloudFormation
    - Imperative: Ansible, Shell scripts
  - Core Concepts:
    - Version control
    - Automation
    - Idempotency
    - State management
  - Related to: DevOps, GitOps

- **GitOps**
  - Git as single source of truth
  - Principles:
    - Declarative system
    - Immutability
    - Pull-based deployment
    - Version control
  - Components:
    - Repository structure
    - Deployment operators
    - Environment management
    - Change workflows
  - Tools:
    - Flux CD
    - ArgoCD
    - Jenkins X
    - Tekton

- **Container Orchestration**
  - Managing containerized applications
  - Features:
    - Scheduling
    - Load balancing
    - Service discovery
    - Health monitoring
  - Tools:
    - Kubernetes
    - Docker Swarm
    - Nomad

### Data
- **Data Storage Patterns**
  - Row-oriented: Traditional RDBMS
  - Column-oriented: Analytics databases
  - Document-oriented: JSON/XML storage
  - Key-value: Simple lookup
  - Graph: Relationship-focused
  - Time-series: Sequential data
  - Object storage: Binary data

- **Database Concepts**
  - ACID Properties:
    - Atomicity: All or nothing
    - Consistency: Valid state transitions
    - Isolation: Transaction separation
    - Durability: Permanent changes

  - CAP Theorem:
    - Consistency: All nodes synchronized
    - Availability: Always responsive
    - Partition tolerance: Handles network issues
    - Trade-offs between properties

  - Normalization:
    - 1NF: Atomic values
    - 2NF: Full functional dependency
    - 3NF: No transitive dependency
    - BCNF: Every determinant is a key

- **Data Integration**
  - ETL/ELT Processes
  - Data Warehousing
  - Data Lakes
  - Master Data Management
  - Data Quality Management

- **Data Serialization**
  - Formats:
    - JSON: Web-friendly, human-readable
    - XML: Document-oriented, schema support
    - YAML: Configuration-focused
    - Protobuf: Efficient binary format
    - Avro: Schema evolution support
  - Schema Definition:
    - JSON Schema
    - XML Schema (XSD)
    - OpenAPI/Swagger
    - GraphQL Schema

## Cross-cutting Concepts
### Security
- **Zero Trust**
  - Verification for all users/devices
  - Components:
    - Identity verification
    - Device validation
    - Access control
    - Network segmentation
  - Related to: Security Architecture

- **Privacy By Design**
  - Proactive privacy measures
  - Key principles:
    - Privacy as default
    - End-to-end security
    - Full lifecycle protection
    - Transparency
  - Related to: GDPR, AI Act

- **IEC/ISO27001**
  - Security standard for organizations
  - Coverage:
    - Risk assessment
    - Security controls
    - Management system
    - Continuous improvement

### Implementation & Integration
- **Documentation as Code**
  - Documentation in version control
  - Tools:
    - Markdown
    - AsciiDoc
    - PlantUML/Mermaid
    - Sphinx
  - Practices:
    - Automated validation
    - Review process
    - Continuous integration
  - Related to: DevOps, GitOps

- **API Gateway**
  - API management frontend
  - Features:
    - Request routing
    - Authentication
    - Rate limiting
    - Transformation
  - Related to: Microservices

- **Message Queue**
  - Asynchronous communication
  - Patterns:
    - Point-to-point
    - Publish-subscribe
    - Request-reply
    - Dead letter queue
  - Related to: Event-Driven Architecture

- **Feature Toggle/Flag**
  - Runtime functionality control
  - Types:
    - Release toggles
    - Experiment toggles
    - Ops toggles
    - Permission toggles
  - Related to: Continuous Delivery

### Modeling & Documentation
- **UML (Unified Modeling Language)**
  - Comprehensive modeling notation
  - Diagram types:
    - Class diagrams
    - Sequence diagrams
    - State diagrams
    - Activity diagrams
    - Component diagrams
    - Deployment diagrams

- **ArchiMate**
  - Enterprise architecture modeling
  - Layers:
    - Business
    - Application
    - Technology
  - Aspects:
    - Active structure
    - Behavior
    - Passive structure
  - Cross-cutting:
    - Strategy
    - Physical
    - Implementation