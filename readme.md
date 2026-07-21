# Azure RMF Accelerator JSON

The canonical JSON schema and reference implementation for **Azure RMF Accelerator**.

This repository contains the foundational data model used to normalize Azure, Infrastructure-as-Code (IaC), security, Power Platform, and Copilot workload metadata into a standardized format for RMF artifact generation.

## Purpose

RMF accreditation requires the creation and maintenance of numerous artifacts, including:

- System Design Specification Documents (SDSD)
- System Security Plans (SSP)
- System Requirements Traceability Matrices (SRTM)
- Hardware / Software Asset Lists
- Ports, Protocols, and Services (PPS)
- Software Bills of Materials (SBOM)
- Test & Evaluation Documentation
- eMASS Import Content

Many of the facts required to populate these artifacts already exist within cloud resources, infrastructure definitions, security configurations, and application metadata.

This repository defines a canonical JSON model that serves as the authoritative intermediary between technical implementations and RMF documentation.

```text
Bicep
Terraform
Azure Resources
Azure Policy
Defender
Power Platform
Copilot Studio

        ↓

RMF JSON Schema

        ↓

Artifact Generators

        ↓

SDSD
SSP
SRTM
PPS
SBOM
Inventories
eMASS Imports
```

## Design Principles

### Deterministic First

The schema is designed to capture authoritative technical facts.

Generated artifacts should be based on:

- Infrastructure-as-Code
- Azure Resource Metadata
- Security Configurations
- Application Definitions

rather than free-form AI generation.

### Traceable

Every generated artifact should be traceable back to an authoritative source.

### Reusable

A single normalized data model supports multiple RMF artifacts.

### Extensible

The schema is intended to evolve as additional artifact generators and data sources are added.

## Repository Contents

```text
.
├── schema/
│   └── ara.schema.json
│
├── examples/
│   └── simple-system.json
│
└── README.md
```

### ara.schema.json

Defines the Azure RMF Accelerator canonical data model.

### simple-system.json

Reference implementation demonstrating schema usage.

### README.md

Project documentation and design guidance.

## Current Schema Areas

The initial schema includes:

- Roles
- Azure Resources
- Test Definitions

Future schema areas may include:

- System Metadata
- Authorization Boundaries
- Controls
- Security Findings
- Ports / Protocols / Services
- Software Inventories
- Data Flows
- Privacy Information
- SBOM Definitions
- Evidence Mappings

## AI Usage

Azure RMF Accelerator is not intended to rely on AI for authoritative data generation.

AI is intended to assist with:

- Component descriptions
- Technical explanations
- Architecture narratives
- Control implementation language
- Documentation readability

Authoritative technical metadata remains the source of truth.

## Vision

**Infrastructure-as-Code for RMF Documentation**

By establishing a common RMF data model, Azure RMF Accelerator seeks to reduce manual documentation effort, improve artifact consistency, and enable repeatable generation of accreditation content from cloud-native implementations.

## License

This project is licensed under the MIT License.