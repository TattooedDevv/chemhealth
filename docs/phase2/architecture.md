# Phase 2 — System Design: Architecture

## 1. Architecture Overview

ChemHealth is a web-based platform that combines computational chemistry analysis and machine learning to evaluate medications, hormones, and supplements related to women’s health.

The system is designed using a modular architecture with clear separation between the user interface, backend API, analysis/ML logic, and data storage.

## 2. Key Components

### 2.1 Frontend (Web UI)
- Provides the user interface for dataset upload, exploration, visualizations, and report download
- Communicates with the backend through REST API calls

### 2.2 Backend API
- Handles request validation and routing
- Orchestrates analysis workflows
- Interfaces with external chemistry data sources
- Stores/retrieves datasets and results

### 2.3 Analysis & Machine Learning Engine
- Performs chemical property calculations (e.g., solubility-related features)
- Generates model inputs (feature engineering)
- Produces predictions and metrics for display

### 2.4 Database
- Stores molecular datasets and metadata
- Stores analysis results and reports
- Stores user preferences/auth data (planned)

## 3. External Integrations (Planned/Optional)
- PubChem, ChEMBL, and literature-based references for molecular/chemical properties

## 4. Diagram References

- System Architecture: `diagrams/system-architecture.png`
- Deployment Environment: `diagrams/deployment-environment.png`
- Azure Target Architecture (Optional): `diagrams/azure-architecture.png`

## 5. Design Rationale

This architecture was selected to:
- Keep UI, API, and analysis logic decoupled
- Support future scaling and cloud deployment
- Allow independent iteration on ML models and data pipelines
