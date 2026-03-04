# Phase 3 — Stack Selection

## 1. Overview

This document finalizes the technology stack for ChemHealth based on the architectural decisions made in Phase 2. Each selection is justified against the project's functional and non-functional requirements.

---

## 2. Frontend

### 2.1 Framework & Language

- React 18.x — component-based UI, strong ecosystem, ideal for dashboards and data visualization
- JavaScript (ES2022+) — primary frontend language

### 2.2 UI Component Library

- MUI (Material UI) v5 — pre-built component library providing consistent design, accessible components, and built-in data grid and chart support for the analysis dashboard
- Motion (Framer Motion) — animation library for React; used for page transitions, dashboard element reveals, and interactive UI feedback alongside MUI components

---

## 3. Backend

### 3.1 Runtime & Framework

- Python 3.11+ — strong ML/data ecosystem, maintainability
- FastAPI — async-first REST API framework with built-in OpenAPI/Swagger documentation and native request validation via Pydantic

---

## 4. Data Science / Machine Learning

### 4.1 Core Libraries

- NumPy — numerical computation and array operations
- Pandas — data manipulation and dataset handling
- Scikit-learn — baseline classification and regression models for solubility and absorption prediction (FR4, FR5)

---

## 5. Database

### 5.1 Primary Database

- PostgreSQL 16.x — relational structure fits molecular datasets, analysis results, and user metadata; satisfies NFR3 through foreign key constraints and transactional guarantees

---

## 6. DevOps / Infrastructure

### 6.1 Containerization

- Docker — packages each service into isolated, reproducible containers
- Docker Compose — orchestrates the full local stack (frontend, backend, PostgreSQL) during development, satisfying NFR5

### 6.2 CI/CD

- Jenkins — pipeline automation for build, test, and deployment stages
- GitHub Actions — source control integrated CI/CD for automated checks on pull requests and branch pushes
