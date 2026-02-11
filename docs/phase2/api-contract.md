# API Contract — ChemHealth

## Purpose

This document defines the high-level API contract between the frontend and backend services of the ChemHealth platform.
It establishes request/response expectations prior to implementation.

## Design Principles

- REST-based communication
- JSON request and response bodies
- Clear separation between UI and analysis logic
- Versionable endpoints

## Core Endpoints (Planned)

### Dataset Management

POST /api/datasets
- Description: Upload molecular dataset
- Request: Dataset file + metadata
- Response: Dataset ID, status

GET /api/datasets
- Description: Retrieve available datasets
- Response: Dataset list

### Analysis

POST /api/analyze
- Description: Run chemical analysis and ML prediction
- Request: Dataset ID + analysis parameters
- Response: Job ID, status

GET /api/results/{id}
- Description: Retrieve analysis results
- Response: Metrics, predictions, visual data

### Reports

GET /api/reports/{id}
- Description: Download analysis report
- Response: PDF or structured data

## Authentication (Planned)

- Authentication and authorization will be added in later phases
- Initial development assumes trusted users

## Versioning

- API versioning will be applied using URL-based versioning (e.g., /api/v1)
