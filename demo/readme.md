
**Anirudh**

```
  ├── Implement Dev/QA infra via tf Modules
  │     ├── Terraform module CI
  │     │     └── Implementation
  │     ├── Terraform module CD
  │     │     └── Implementation
  │     ├── DSL Jenkins pipeline for Dev Env
  │     │     ├── Network skeleton setup (Dev)
  │     │     ├── ScyllaDB setup (Dev)
  │     │     ├── Redis setup (Dev)
  │     │     └── PostgreSQL setup (Dev)
  │     └── Wrapper code for QA Env
  │           ├── Network skeleton setup (QA)
  │           ├── ScyllaDB setup (QA)
  │           ├── Redis setup (QA)
  │           └── PostgreSQL setup (QA)
  └── Design CD
        └── Detailed analysis on mutable/immutable infra
               └── Mutable Infra
```

**Anitha**


  ├── Design Monitoring
  │     ├── Design Infra Monitoring
  │     │     ├── Identify Key Performance Metrics (Documentation)
  │     │     ├── Dashboard Designing (Documentation)
  │     │     ├── Alerting Rules & Process using AlertManager (Documentation)
  │     │     └── Metrics Achievement (POC)
  │     └── Design Logs Monitoring
  │           ├── Key Metrics Identification (Documentation)
  │           └── Alerting Rules for Logs (Documentation)
  ├── IAC Unit Test (Beyond Expectation)
  │     └── Ansible
  │           ├── Ansible Unit Test (Documentation)
  │           └── Ansible Unit Test (POC)
  └── Infrastructure GitOps (Beyond Expectation)
        └── Terraform Infra Divergence
              ├── Divergence Management (Understanding)
              └── Divergence Management (POC)



**Himanshu**

  ├── Implement Dev/QA Infra via tf Modules
  │     ├── DSL Jenkins Pipeline for Dev Env
  │     │     ├── Frontend Setup (Dev)
  │     │     ├── Attendance Setup (Dev)
  │     │     ├── Employee Setup (Dev)
  │     │     ├── Salary Setup (Dev)
  │     │     └── Notification Setup (Dev)
  │     └── Wrapper Code for QA Env
  │           ├── Frontend (QA)
  │           ├── Attendance App (QA)
  │           ├── Employee App (QA)
  │           ├── Salary App (QA)
  │           └── Notification (QA)
  └── Design CD
        └── Deployment Strategies
              └── Documentation



**Pravalika**

  ├── Design Monitoring
  │     ├── Design ScyllaDB & PostgreSQL Monitoring
  │     │     ├── Documentation: Identify Key Performance Metrics & Requirements
  │     │     ├── Documentation: Dashboard Designing
  │     │     ├── Documentation: Alerting Rules & Process
  │     │     └── POC: Achieving Metrics for DB Monitoring
  │     └── Design Logs Monitoring
  │           ├── Documentation: Dashboard Designing for App Logs
  │           └── POC: Achieving Metrics for App Logs Monitoring
  ├── Terragrunt (Beyond Expectation)
  │     ├── Documentation: TerraGrunt
  │     └── POC: TerraGrunt Implementation
  └── IAC Unit Test (Beyond Expectation)
        └── Terraform
              ├── Documentation: Terraform Unit Test
              └── POC: Terraform Unit Test


**Shrey**

  ├── Implement Dev/QA Infra via tf Modules
  │     ├── Shared Library for tf Wrapper Code Execution
  │     │     ├── Documentation
  │     │     └── POC
  │     └── DSL Jenkins Pipeline for QA
  │           ├── Network Skeleton Setup (QA)
  │           ├── Frontend Setup (QA)
  │           ├── Attendance Setup (QA)
  │           ├── Employee Setup (QA)
  │           └── Salary Setup (QA)
  └── Infrastructure GitOps (Beyond Expectation)
        └── Terraform GitOps
              ├── Understanding
              ├── Tools
              └── POC

**Shubham**

  ├── Design CD
  │     ├── Deployment Strategies
  │     │     └── Documentation
  │     └── Design Document for Immutable Infra Rollout
  │           └── Canary
  └── Design Monitoring
        ├── Design App Monitoring
        │     ├── Documentation: Key Performance Metrics & Requirements
        │     ├── Documentation: Dashboard Designing (Applications)
        │     ├── Documentation: Alerting Rules & Process via AlertManager
        │     └── POC: Achieving Metrics for App Monitoring
        └── Design Redis Monitoring
              ├── Documentation: Key Performance Metrics & Requirements (Middleware)
              ├── Documentation: Dashboard Designing (Middleware)
              ├── Documentation: Alerting Rules & Process (Middleware)
              └── POC: Achieving Metrics for Middleware Monitoring


**Tharik**


  ├── Implement Dev/QA Infra via tf Modules
  │     ├── Shared Library for Terraform Module CI/CD
  │     │     ├── Documentation
  │     │     └── POC
  │     └── DSL Jenkins Pipeline for QA
  │           ├── Notification Setup (QA)
  │           ├── ScyllaDB Setup (QA)
  │           ├── Redis Setup (QA)
  │           └── PostgreSQL Setup (QA)
  └── Design CD
        └── Design Document for Immutable Infra Rollout
              ├── Blue Green Strategy
              └── Rolling Strategy
**Rajeev**

  └── Implement Dev/QA Infra via tf Modules
        ├── Terraform Module for Standalone VM
        │     ├── Subtasks: Create module for standalone VM
        │     ├── Acceptance: Static IP, naming conventions, metadata tags
        │     ├── Comment: Demo for review
        │     └── Assignee: Rajeev
        ├── DSL Jenkins Pipeline
        │     ├── Subtasks: Create pipeline for app provisioning
        │     ├── Acceptance: Folders per module, standard naming, parameters
        │     ├── Comment: Jenkins integration demo
        │     └── Assignee: Rajeev
        └── Wrapper Code for Dev Env
              ├── Subtasks: App-specific wrapper scripts (attendance, salary, etc.)
              ├── Acceptance: CLI-based execution, folder standards
              ├── Comment: Wrapper logic demo
              └── Assignee: Rajeev
**Aditya**

  └── Implement Dev/QA Infra via tf Modules
        ├── Terraform Module: Network Skeleton
        │     ├── Sub Task: Create module for network skeleton
        │     ├── Acceptance Criteria:
        │     │     - Align setup with dev/qa infra diagram
        │     │     - Use proper naming conventions by environment
        │     │     - Maintain logical directory structure
        │     ├── Comment:
        │     │     - Demo for Pre & LO reviewers
        │     │     - Use central account, not personal
        │     └── Assignee: Aditya
        ├── Terraform Module: Autoscaling Setup
        │     ├── Sub Task: Create module for autoscaling
        │     ├── Acceptance Criteria:
        │     │     - CI stages via shared lib: init, validate, plan
        │     │     - Clear execution logs
        │     ├── Comment: PR review + demo
        │     └── Assignee: Aditya
        ├── DSL Jenkins Pipeline (CI/CD)
        │     ├── CI for Network Skeleton
        │     ├── CI for Autoscaling
        │     ├── CD for Network Skeleton
        │     └── CD for Autoscaling
        │     ├── Acceptance Criteria:
        │     │     - Use shared lib for all stages (init → destroy)
        │     │     - Clear logs across pipeline
        │     ├── Comment: PR review + demo
        │     └── Assignee: Aditya
        ├── Wrapper Code for Dev Environment
        │     ├── For Network Skeleton
        │     ├── For Frontend
        │     └── For Salary App
        │     ├── Acceptance Criteria:
        │     │     - CLI-based deployment with standard variables/tags
        │     │     - No execution errors
        │     ├── Comment: PR review + demo
        │     └── Assignee: Aditya
        └── DSL Jenkins Pipeline for Dev Setup
              ├── Network Skeleton
