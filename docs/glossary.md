# ADR Glossary

## Architectural Decision Records (ADR) Concepts

- Architecture Decision Record (ADR)
  - A documented record of a significant architectural decision.
  - Related to: Decision Log, Design Documentation

- Architecture Decision Log (ADL)
  - A collection of all ADRs for a project.
  - Also known as: Decision History, Architecture Changelog

- Decision Story
  - Narrative describing the context and reasoning behind an architectural decision
  - Related to: Context, Rationale, RCDA

## Architectural Patterns & Concepts

- Event Sourcing
  - Pattern where state changes are stored as a sequence of events
  - Also known as: Event Store Pattern
  - Related to: CQRS, Event-Driven Architecture

- Long-Lived Transactions (LLT)
  - Transactions that span multiple system boundaries or time periods
  - Also known as: Saga Pattern, Choreography-based Transactions
  - Related to: Compensating Transactions, Distributed Transactions

- CQRS (Command Query Responsibility Segregation)
  - Pattern separating read and write operations
  - Related to: Event Sourcing, Domain-Driven Design

- Service Mesh
  - Infrastructure layer for service-to-service communication
  - Also known as: Network Fabric
  - Related to: Service Discovery, Load Balancing

- Microservices
  - Architectural style structuring an application as a collection of loosely coupled services
  - Related to: Service-Oriented Architecture, Distributed Systems

- Domain-Driven Design (DDD)
  - Approach to software development focusing on the core domain
  - Related to: Bounded Contexts, Ubiquitous Language

- Bounded context
  - Basically the ability to group something and use that to abstract other factors out
  - Related to: Domain-Driven Design

- RCDA
  - Risk- and Cost-Driven Architecture (RCDA) is an architecting approach developed by CGI that focuses on managing risks and costs in solution design. 
  - Key aspects:
   - Decision Stories
   - Risk-first approach to solution design
   - Cost optimization and management
   - Scalable methodology
   - Agile and deadline-oriented
   - Validated through peer-reviewed research
   - Recognized by Open Group Certified Architect (OpenCA) program
  - Related to: Decision Stories

- Decision Stories
  - Method to document architectural choices in a standardized and transparent way
   - In the context of: [current situation/project/environment]
   - Facing concern(s): [list key problems/challenges]
   - We decided: [chosen solution/approach]
   - And not: [rejected alternatives]
   - To achieve: [expected outcomes/benefits]
   - Accepting: [trade-offs/consequences]

- TOGAF
  - The Open Group Architecture Framework is an enterprise architecture methodology and framework that helps organizations design, plan, implement, and govern enterprise IT architecture. 
  - Its core component is the Architecture Development Method (ADM), a repeatable cycle for developing architecture.
   - Preliminary: Defines how to implement TOGAF within the organization
   - Architecture Vision: Sets project scope, constraints, and expectations
   - Business Architecture: Describes current business structure and goals
   - Information Systems Architecture: Covers data and application architecture
   - Technology Architecture: Describes software and hardware infrastructure
   - Opportunities and Solutions: Initial implementation planning
   - Migration Planning: Cost-benefit analysis and detailed implementation plan
   - Implementation Governance: Provides architectural oversight
   - Architecture Change Management: Monitors and manages changes

## Domain Modeling Concepts

- Bounded Context
  - A specific responsibility with explicit boundaries that represents a specialized domain model
  - Also known as: Context Boundary, Domain Boundary
  - Key concepts:
    - Shared Kernel:
    - Model shared between two bounded contexts
    - Context Map: Document showing relationships between bounded contexts
    - Anti-corruption Layer: Interface layer protecting one bounded context from another
    - Upstream/Downstream: Relationship pattern between bounded contexts
  - Related to: Domain-Driven Design, Microservices

- Context Mapping
  - Practice of documenting relationships between bounded contexts
  - Types:
   - Partnership: Teams agree to coordinate changes
   - Customer/Supplier: Upstream/downstream relationship
   - Conformist: Downstream team uses upstream model
   - Anti-corruption Layer: Downstream team translates upstream model
   - Open Host Service: Upstream provides protocol for integration
   - Published Language: Formal schema for context communication
  - Related to: System Integration, Domain-Driven Design

- Ubiquitous Language
  - Common, rigorous language within a bounded context
  - Characteristics:
   - Shared by all team members (technical and domain experts)
   - Precise within the bounded context
   - May have different meanings in other contexts
  - Related to: Domain-Driven Design, Requirements Engineering

## System Quality Attributes

- Scalability
  - System's ability to handle growing amounts of work
  - Types: Vertical (Scale Up), Horizontal (Scale Out)

- Reliability
  - System's ability to perform specified functions under stated conditions
  - Related to: Availability, Fault Tolerance

- Maintainability
  - Ease with which a system can be modified to correct faults, improve performance
  - Related to: Technical Debt, Code Quality

- Performance
  - System's response time, throughput, and resource usage characteristics
  - Related to: Latency, Throughput, Efficiency

## Development Concepts

- Technical Debt
  - Implied cost of additional rework caused by choosing an easy solution now
  - Types: Deliberate, Accidental
  - Related to: Refactoring, Code Quality

- Coupling
  - Degree of interdependence between software modules
  - Types: Tight, Loose
  - Related to: Cohesion, Modularity

- Cohesion
  - Degree to which elements of a module belong together
  - Types: High, Low
  - Related to: Coupling, Single Responsibility Principle

## Version Control & Release Management

- Breaking Change
  - A change that breaks backward compatibility
  - Also known as: Major Version Change
  - Related to: Semver, Migration Path

- Semver (Semantic Versioning)
  - Version numbering scheme: MAJOR.MINOR.PATCH
  - Example: 1.3.1
  - Related to: Release Management, Compatibility

- Feature Toggle/Flag
  - Technique to enable/disable functionality without code changes
  - Also known as: Feature Switch, Feature Flip
  - Related to: Continuous Delivery, A/B Testing

## Cloud & Infrastructure

- Infrastructure as Code (IaC)
  - Managing infrastructure through code rather than manual processes
  - Related to: Configuration Management, DevOps

- Container Orchestration
  - Automating deployment, scaling, and management of containerized applications
  - Examples: Kubernetes, Docker Swarm(well not really, but it looks stupid with only one example)
  - Related to: Microservices, Cloud Native

- Cloud Native
  - Applications designed specifically for cloud computing
  - Related to: Containers, Microservices, DevOps

## Security & Compliance

- Zero Trust
  - Security concept requiring verification for all users and devices, basically what measure syou would put in place for a system on the internet
  - Related to: Security Architecture, Authentication

- Defense in Depth
  - Layered security strategy
  - Also known as: Layered Security
  - Related to: Security Architecture, Risk Management

- IEC/ISO27001
  - Most commonly used security standard for organisational compliance  

- Privacy By Design
  - An open-ended collection of measures you will adopt in relation to handling data with the purpose of securing integrity, semantic understanding and other factors with the purpose of respecting users rights.
  - Related to: Security Architecture, GDPR, AI Act 

## Integration Patterns

- API Gateway
  - Server that acts as an API front-end
  - Related to: Microservices, Service Mesh

- Message Queue
  - Asynchronous communication mechanism
  - Related to: Event-Driven Architecture, Pub/Sub

## Testing & Quality

- Test-Driven Development (TDD)
  - Development process relying on very short development cycles
  - Related to: Unit Testing, Continuous Integration

- Continuous Integration/Continuous Deployment (CI/CD)
  - Practices of automating building, testing, and deployment
  - Related to: DevOps, Automation

## Architectural Frameworks
 
### Object-Oriented Analysis and Design (OOAD)

- Object-Oriented Analysis (OOA)
  - Process of analyzing a problem domain from object-oriented perspective
  - Key concepts:
    - Objects: Instances of a class representing real-world entities
    - Classes: Templates defining object structure and behavior
    - Inheritance: Mechanism for code reuse and specialization
    - Polymorphism: Ability to present same interface for different implementations
    - Related to: Requirements Engineering, Domain Modeling

- Object-Oriented Design (OOD)
  - Process of designing software system using object-oriented principles
  - Key concepts:
    - Abstraction: Hiding implementation details
    - Encapsulation: Bundling data and methods that operate on that data
    - Association: Relationships between objects
    - Composition: Strong ownership relationship between objects
    - Aggregation: Weak ownership relationship between objects
    - Related to: Software Architecture, Design Patterns

- Design Patterns
  - Reusable solutions to common design problems
  - Categories:
    - Creational: Object creation mechanisms
    - Structural: Object composition and relationships
    - Behavioral: Object communication and responsibility
    - Related to: Gang of Four Patterns, Enterprise Patterns

- SOLID Principles
  - Single Responsibility Principle (SRP)
    - A class should have only one reason to change
      - Key aspects:
      - Focused functionality
      - High cohesion
      - Clear boundaries of responsibility
      - Related to: Separation of Concerns, Maintainability

  - Open/Closed Principle (OCP)
    - Software entities should be open for extension but closed for modification
    - Key aspects:
      - Use interfaces and abstract classes
      - Enable behavior extension without source modification
      - Support plugin architecture
      - Related to: Interface-based Design, Extensibility

  - Liskov Substitution Principle (LSP)
    - Objects of a superclass should be replaceable with objects of subclasses
    - Key aspects:
      - Behavioral compatibility
      - Contract adherence
      - Type safety
      - Related to: Inheritance, Polymorphism

  - Interface Segregation Principle (ISP)
    - Clients should not be forced to depend on interfaces they don't use
    - Key aspects:
      - Small, focused interfaces
      - Role-specific interfaces
      - Avoid fat interfaces
      - Related to: API Design, Modularity

  - Dependency Inversion Principle (DIP)
    - High-level modules should not depend on low-level modules
    - Key aspects:
      - Depend on abstractions
      - Inversion of Control (IoC)
      - Dependency Injection (DI)
      - Related to: Loose Coupling, Dependency Management
  - Common SOLID Violations
    - God Class: Violation of SRP
    - Rigid Hierarchy: Violation of OCP
    - Type Checking: Violation of LSP
    - Fat Interfaces: Violation of ISP
    - Tight Coupling: Violation of DIP
    - Related to: Code Smells, Refactoring

### Code Smells
- Definition
  - Indicators of potential problems in code design or implementation
  - Not necessarily bugs, but opportunities for improvement
  - Often violate design principles or best practices
  - Related to: Technical Debt, Refactoring

### Bloaters
- Long Method
  - Method that has grown too large and complex
  - Signs: Many lines, multiple responsibilities, high cyclomatic complexity
  - Fix: Extract Method, Replace Temp with Query
  - Related to: Single Responsibility Principle

- Large Class
  - Class that has taken on too many responsibilities
  - Signs: Too many fields/methods, low cohesion
  - Fix: Extract Class, Extract Interface, Extract Subclass
  - Related to: God Object Anti-pattern

- Primitive Obsession
  - Overuse of primitive data types for domain concepts
  - Signs: Many primitive fields, string-based enums
  - Fix: Replace Data Value with Object, Extract Class
  - Related to: Value Objects, Domain-Driven Design

- Long Parameter List
  - Method with excessive parameters
  - Signs: More than 3-4 parameters
  - Fix: Introduce Parameter Object, Preserve Whole Object
  - Related to: Method Design

### Change Preventers
- Divergent Change
  - Class that changes for multiple different reasons
  - Signs: Unrelated modifications in same class
  - Fix: Extract Class, Move Method
  - Related to: Single Responsibility Principle

- Shotgun Surgery
  - Single change requires multiple class modifications
  - Signs: Changes scattered across codebase
  - Fix: Move Method, Move Field, Inline Class
  - Related to: Coupling

- Parallel Inheritance Hierarchies
  - Creating a subclass in one hierarchy requires subclass in another
  - Signs: Duplicate inheritance structures
  - Fix: Move Method, Move Field
  - Related to: Inheritance

### Couplers
- Feature Envy
  - Method more interested in another class's data
  - Signs: Method uses many methods/data from another class
  - Fix: Move Method, Extract Method
  - Related to: Law of Demeter

- Inappropriate Intimacy
  - Classes that know too much about each other
  - Signs: Excessive method calls, shared fields
  - Fix: Move Method, Move Field, Replace Inheritance with Delegation
  - Related to: Encapsulation

- Message Chains
  - Series of method calls to navigate object relationships
  - Signs: Long chains like a.getB().getC().getD()
  - Fix: Hide Delegate, Extract Method
  - Related to: Law of Demeter

### Object-Orientation Abusers
- Switch Statements
  - Complex conditional logic that tends to be duplicated
  - Signs: Multiple switch/if based on type
  - Fix: Replace Conditional with Polymorphism
  - Related to: Strategy Pattern

- Temporary Field
  - Class fields used only in certain circumstances
  - Signs: Fields only used by certain methods
  - Fix: Extract Class, Introduce Null Object
  - Related to: Class Design

- Refused Bequest
  - Subclass uses only some methods/properties of superclass
  - Signs: Inherited methods throwing exceptions
  - Fix: Replace Inheritance with Delegation
  - Related to: Liskov Substitution Principle

### Dispensables
- Comments
  - Comments that compensate for bad code
  - Signs: Comments explaining unclear code
  - Fix: Extract Method, Rename Method
  - Related to: Clean Code

- Duplicate Code
  - Same code structure in multiple places
  - Signs: Copy-pasted code, similar code patterns
  - Fix: Extract Method, Pull Up Method, Form Template Method
  - Related to: DRY Principle

- Data Class
  - Classes with only fields and crude methods
  - Signs: No behavior, only getters/setters
  - Fix: Move Method, Encapsulate Field
  - Related to: Encapsulation

## Data & Database Concepts
- Relational Theory
  - Mathematical theory for data management using relations (tables)
  - Key concepts:
    - Relations (Tables): Sets of tuples sharing attributes
    - Tuples (Rows): Individual data entries
    - Attributes (Columns): Properties defining data structure
  - Related to: Database Design, Set Theory

- Relational Operations
  - Select: Filtering rows based on conditions
  - Project: Selecting specific columns
  - Join: Combining relations based on common attributes
  - Union/Intersection: Set operations on relations
  - Related to: SQL, Query Optimization

- Database Normalization
  - Process of organizing data to reduce redundancy
  - Forms:
    - 1NF: Atomic values, no repeating groups
    - 2NF: 1NF + no partial dependencies
    - 3NF: 2NF + no transitive dependencies
    - BCNF: 3NF + every determinant is a candidate key
  - Related to: Data Integrity, Database Design

- Integrity Constraints
  - Entity Integrity: Primary key constraints
  - Referential Integrity: Foreign key constraints
  - Domain Integrity: Valid attribute values
  - Business Rules: Application-specific constraints
  - Related to: Data Quality, Database Design

- Transaction Properties (ACID)
  - Atomicity: All or nothing
  - Consistency: Valid state transitions
  - Isolation: Concurrent transaction separation
  - Durability: Permanent changes
  - Related to: Transaction Management, Data Consistency

- CAP Theorem
  - Consistency: All nodes see same data
  - Availability: Every request receives response
  - Partition Tolerance: System functions despite network issues
  - Related to: Distributed Systems, NoSQL

- Data Storage Patterns
  - Row-oriented: Traditional RDBMS
  - Column-oriented: Analytics databases
  - Document-oriented: JSON/XML storage
  - Key-value: Simple key-based lookup
  - Graph: Relationship-focused storage
  - Related to: Database Types, Use Case Optimization

- Query Processing
  - Query Planning: Optimization strategy
  - Index Usage: Access path selection
  - Join Algorithms: Nested loops, hash joins, merge joins
  - Related to: Performance Optimization, Database Tuning

- Concurrency Control
  - Locking: Pessimistic concurrency control
  - MVCC: Optimistic concurrency control
  - Deadlock Detection: Identifying and resolving conflicts
  - Related to: Transaction Management, Performance

- Data Integration
  - ETL: Extract, Transform, Load
  - ELT: Extract, Load, Transform
  - Data Warehouse: Integrated data repository
  - Data Lake: Raw data storage
  - Related to: Business Intelligence, Analytics

### Data Structuring & Serialization

- Structured Data
  - Data organized according to predefined models or schemas
  - Types:
    - Tables: Row/column format (e.g., CSV, Excel)
    - Hierarchical: Parent-child relationships (e.g., XML)
    - Network: Many-to-many relationships (e.g., Graph data)
  - Related to: Data Modeling, Schema Design

- Data Serialization
  - Process of converting data structures into format for storage/transmission
  - Key aspects:
    - Encoding: Converting to byte streams
    - Decoding: Reconstructing original data
    - Schema Evolution: Managing format changes
  - Related to: Data Integration, APIs

- Common Data Formats
  - JSON (JavaScript Object Notation)
    - Lightweight, human-readable
    - Key-value pairs and arrays
    - Schema-optional
    - Common in: Web APIs, Document DBs
    
  - XML (eXtensible Markup Language)
    - Tag-based hierarchical structure
    - Schema support (XSD)
    - Namespaces for disambiguation
    - Common in: SOAP APIs, Config files

  - YAML (YAML Ain't Markup Language)
    - Human-readable format
    - Supports references and aliases
    - Indentation-based structure
    - Common in: Configuration, Docker

  - Protocol Buffers (Protobuf)
    - Binary serialization format
    - Schema-required (proto files)
    - Language-neutral
    - Common in: gRPC, High-performance systems

  - Avro
    - Binary serialization format
    - Schema evolution support
    - Dynamic typing
    - Common in: Hadoop, Big Data

- Schema Definition Languages
  - JSON Schema
    - Validates JSON documents
    - Type checking and constraints
    - Documentation generation
    
  - XSD (XML Schema Definition)
    - Defines XML structure
    - Type system and validation
    - Namespace management

  - OpenAPI/Swagger
    - REST API definition
    - Request/response schemas
    - API documentation

- Data Exchange Patterns
  - Message Formats
    - Headers: Metadata and routing info
    - Payload: Actual data content
    - Envelope: Wrapping structure
    
  - Content Negotiation
    - Format selection
    - Version management
    - Compression options

  - Transformation
    - Format conversion
    - Schema mapping
    - Data validation

## As Code

### Documentation as Code
- Definition
  - Practice of treating documentation like source code
  - Documentation stored alongside code in version control
  - Uses same tools and workflows as development
  - Related to: DevOps, Continuous Integration

- Core Principles
  - Version Control
    - Documentation in git repositories
    - Branch strategies
    - Pull request reviews
    - History tracking
  
  - Automation
    - Automated builds
    - Validation checks
    - Publication pipelines
    - Link checking
  
  - Formats
    - Markdown: Human-readable text format
    - AsciiDoc: Rich text documentation
    - reStructuredText: Python documentation standard
    - OpenAPI: API documentation
    - PlantUML/Mermaid: Diagrams as code

- Testing & Validation
  - Link validation
  - Syntax checking
  - Style guide compliance
  - Code snippet testing
  - API documentation testing
  - Related to: Continuous Integration, Quality Assurance

- Integration Patterns
  - Code Comments to Docs
  - API Specs to Documentation
  - Architecture Diagrams as Code
  - Test Cases as Documentation
  - ADRs in Version Control
  - Related to: DevOps Pipeline, CI/CD

- Documentation Platforms
  - Static Site Generators
    - Jekyll, Hugo, MkDocs
    - Build from source formats
    - Theme customization
  - Documentation Hosting
    - GitHub Pages
    - ReadTheDocs
    - Documentation Portals
  - Related to: Content Management, Web Hosting

### Policy as Code
- Definition
  - Practice of expressing policies in machine-readable format
  - Automated enforcement of rules and standards
  - Version-controlled policy definitions
  - Related to: Infrastructure as Code, Security as Code

- Implementation Patterns
  - Policy Languages
    - Rego (OPA): Policy language for Cloud Native
    - HCL (Sentinel): HashiCorp policy framework
    - IAM Policies: Access control definitions
    - YAML/JSON: Configuration-based policies
  - Related to: Access Control, Compliance

- Common Use Cases
  - Security Policies
    - Access control rules
    - Network security policies
    - Data protection requirements
    - Compliance checks
  
  - Infrastructure Policies
    - Resource configuration rules
    - Deployment constraints
    - Cost management policies
    - Performance requirements

  - Development Policies
    - Code quality rules
    - Architecture compliance
    - Dependency management
    - Build and deployment rules

- Policy Enforcement Points
  - Pre-deployment
    - Infrastructure planning
    - Code review
    - Build pipeline
  
  - Runtime
    - Request authorization
    - Resource access
    - Configuration changes
  
  - Post-deployment
    - Compliance monitoring
    - Audit logging
    - Policy violation detection

- Policy Testing
  - Unit Testing
    - Individual rule validation
    - Edge case coverage
    - Policy composition
  
  - Integration Testing
    - Policy enforcement validation
    - System interaction testing
    - Performance impact

- Policy Management
  - Version Control
    - Policy history
    - Change tracking
    - Review process
  
  - Distribution
    - Policy deployment
    - Updates and rollback
    - Environment management
  
  - Monitoring
    - Enforcement tracking
    - Violation detection
    - Effectiveness metrics

### Infrastructure as Code (IaC)

- Definition
  - Practice of managing infrastructure using code and automation
  - Version-controlled infrastructure definitions
  - Automated provisioning and configuration
  - Related to: DevOps, GitOps, Continuous Deployment

- Core Concepts
  - Declarative IaC
    - Describes desired end state
    - System determines required changes
    - Examples: Terraform, CloudFormation
    - Idempotent operations
  
  - Imperative IaC
    - Defines specific steps
    - Script-based approach
    - Examples: Ansible, Shell scripts
    - Procedural execution

- Implementation Patterns
  - Provisioning
    - Resource creation/deletion
    - Infrastructure lifecycle
    - State management
    - Dependencies handling
  
  - Configuration Management
    - Software installation
    - System settings
    - Service configuration
    - State enforcement
  
  - Orchestration
    - Coordination of services
    - Deployment sequencing
    - Service discovery
    - Load balancing

- Best Practices
  - Immutable Infrastructure
    - No in-place updates
    - Complete redeployment
    - Version tracking
    - Rollback support
  
  - Infrastructure Testing
    - Unit tests
    - Integration tests
    - Compliance checks
    - Security scanning
  
  - State Management
    - State file handling
    - Remote state storage
    - State locking
    - Backup strategies

- Common Tools
  - Provisioning Tools
    - Terraform: Multi-cloud provisioning
    - CloudFormation: AWS native
    - ARM Templates: Azure native
    - Pulumi: Programming languages for IaC
  
  - Configuration Management
    - Ansible: Agentless configuration
    - Chef: Ruby-based configuration
    - Puppet: Declarative configuration
    - Salt: Event-driven orchestration

- Security & Compliance
  - Secret Management
    - Credential handling
    - Key rotation
    - Access control
  
  - Compliance
    - Policy enforcement
    - Audit trails
    - Regulatory requirements
    - Security baselines

### GitOps
- Definition
  - Operational practice using Git as single source of truth
  - Declarative infrastructure and application configuration
  - Pull-based deployment model
  - Related to: DevOps, Infrastructure as Code, CI/CD

- Core Principles
  - Declarative System
    - Entire system described declaratively
    - Version controlled configurations
    - Desired state specification
    - Self-documenting systems
  
  - Immutability
    - Immutable infrastructure
    - Version-controlled changes
    - No direct environment modifications
    - Reproducible deployments

  - Pull vs Push
    - Pull-based deployment model
    - Operators watching for changes
    - Automatic drift detection
    - Self-healing systems

- Implementation Patterns
  - Repository Structure
    - Application code
    - Infrastructure definitions
    - Environment configurations
    - Deployment manifests
  
  - Deployment Operators
    - Kubernetes operators
    - Configuration watchers
    - State reconciliation
    - Automated rollback

  - Environment Management
    - Multi-environment support
    - Promotion workflows
    - Configuration inheritance
    - Environment-specific overrides

- GitOps Workflows
  - Change Management
    - Pull requests for changes
    - Code review process
    - Automated validation
    - Change approval flows
  
  - Continuous Deployment
    - Automated deployments
    - Progressive delivery
    - Canary deployments
    - Blue-green deployments

  - Drift Detection
    - State monitoring
    - Automated reconciliation
    - Drift alerts
    - Recovery procedures

- Common Tools
  - Kubernetes-native
    - Flux CD: Progressive delivery
    - ArgoCD: Declarative GitOps
    - Jenkins X: Cloud-native CI/CD
    - Tekton: Cloud-native pipelines
  
  - Supporting Tools
    - Helm: Package management
    - Kustomize: Configuration customization
    - Sealed Secrets: Secret management
    - Prometheus: Monitoring

## Organizational Anti-patterns

- Project Blindness
  - The unintended consequences of breeding enterprise IT development from projects with individual goals
  - Key symptoms:
    - Local optimization at cost of enterprise benefits
    - Duplicate functionality across systems
    - Inconsistent technology choices
    - Fragmented architecture
    - Silos of knowledge
  - Root causes:
    - Project-based funding models
    - Short-term success metrics
    - Lack of enterprise architecture governance
    - Missing cross-project coordination
  - Related to: Technical Debt, Enterprise Architecture

- Conway's Law
  - Systems mirror communication structure of organization
  - Impact on:
    - System architecture
    - Team boundaries
    - Integration patterns
  - Related to: Organization Design, System Architecture

- Project-Product Mismatch
  - Tension between project-based delivery and product-based maintenance
  - Manifestations:
    - Handover problems
    - Maintenance funding gaps
    - Missing long-term ownership
  - Related to: Project Blindness, Technical Debt

- Enterprise Technical Debt
  - Accumulation of suboptimal decisions across projects
  - Sources:
    - Project time pressure
    - Missing enterprise standards
    - Insufficient architecture governance
    - Local optimization
  - Related to: Project Blindness, Architecture Governance

- Scaled Agile
  - An attempt to merge SCRUM and AGILE Values with enterprise wide management.
    - antipatterns include: ad hoc planning coming at odds with architecture goal architecture, developers being pooled into meetings about immature business goal with non-technical people. As well as waterfall planning witout analysis.
  - Related to: Conways Law, Agile Manifesto

- SCRUM
  - An effort to make approximately 5 developers collaborate on the same project in a self-organizing manner
    - Can work if you have the luxury of having a SCRUM master with an understanding of development that can shield the team from organizational noise and interruptions.
    - antipatterns include: micromanagement, removal of self-organization, focus on management tooling and non-code-producing activities
  - Related to: Conways Law, Agile Manifesto
 
- Business Owner
  - A person with domain knowledge put in charge of prioritizing a development teams products.
  - Related to: Conway Law, Agile Manifesto 
 
- Agile Manifesto
  - The agile manifesto reads:
    - We are uncovering better ways of developing software by doing it and helping others do it. Through this work we have come to value:
      - Individuals and interactions over processes and tools
      - Working software over comprehensive documentation
      - Customer collaboration over contract negotiation
      - Responding to change over following a plan
  - Related to: Conways Law

## Common Terms Used in ADRs
- Unified Modelling Language(UML)
  - A detailed modelling language containing class diagrams, sequence diagrams etc.  
- Archimate
  - A modelling language emphasizing Enterprise Architecture
- Feature Toggle/Flag
- RFC 2219
  - The standard for expressing unambigous iformation about requirements specification.
    - MUST This word, or the terms "REQUIRED" or "SHALL", mean that the definition is an absolute requirement of the specification.
    - MUST NOT This phrase, or the phrase "SHALL NOT", mean that the definition is an absolute prohibition of the specification.
    - SHOULD This word, or the adjective "RECOMMENDED", mean that there may exist valid reasons in particular circumstances to ignore a particular item, but the full implications must be understood and carefully weighed before choosing a different course.
    - SHOULD NOT   This phrase, or the phrase "NOT RECOMMENDED" mean that there may exist valid reasons in particular circumstances when the particular behavior is acceptable or even useful, but the full implications should be understood and the case carefully weighed before implementing any behavior described with this label.
    - MAY This word, or the adjective "OPTIONAL", mean that an item is truly optional.
- Related to: https://datatracker.ietf.org/doc/html/rfc2119
- YAGNI
  - 'You Aint Gonna Need It' principle adresses the antipattern of writing placeholders or preparing extensions to codebases with to imminent presence of a need.
