# Development Log

This document records the development process of the **Finance Analytics Automation** project.

The purpose of this log is to document:

- what was done,
- how it was done,
- why each step was necessary,
- and what was learned during the development process.

---

# Day 1 – Project Foundation

**Date:** 2026-07-11

## 1. Project Idea

The project was created as an end-to-end finance analytics and process automation project.

The goal is to build a practical system that combines technologies relevant to finance data analytics, data engineering, automation, and business applications.

The planned technology stack includes:

- Python
- SQL
- dbt
- Snowflake
- Power BI
- Power Platform

The project will be developed step by step and managed as a structured software and data project.

---

## 2. GitHub Repository

A new GitHub repository was created.

**Repository name:**

```text
finance-analytics-automation
```

**Description:**

```text
End-to-end finance analytics and process automation platform using Python, SQL, dbt, Snowflake, Power BI and Power Platform.
```

GitHub is used for:

- source code management,
- version control,
- tracking changes,
- maintaining the project history,
- and publishing the project portfolio.

The repository was created without automatically generating initial files so that the project structure could be created manually and understood step by step.

---

## 3. Local Development Environment

A dedicated Python virtual environment was created.

```bash
python3 -m venv .venv
```

This creates an isolated Python environment inside the `.venv` directory.

### Why?

The virtual environment keeps project dependencies separate from the system Python installation.

This prevents dependency conflicts between different Python projects.

---

## 4. Activate the Virtual Environment

The virtual environment was activated with:

```bash
source .venv/bin/activate
```

After activation, the `python` and `pip` commands use the Python environment inside `.venv`.

---

## 5. Install Initial Python Dependencies

The initial Python packages were installed:

```bash
pip install pandas numpy faker pytest
```

### Installed packages

#### pandas

Used for:

- data loading,
- data transformation,
- tabular data processing,
- and data analysis.

#### numpy

Used for:

- numerical calculations,
- array operations,
- and mathematical data processing.

#### faker

Used to generate synthetic test data.

This will later allow the project to simulate finance-related data without using confidential or real company data.

#### pytest

Used for automated testing.

It allows project functionality to be tested automatically and helps detect errors when the code changes.

---

## 6. Save Python Dependencies

The installed Python dependencies were saved with:

```bash
pip freeze > requirements.txt
```

This creates a `requirements.txt` file containing the installed packages and their versions.

### Why?

The file makes the Python environment reproducible.

Another developer or deployment environment can install the same dependencies using:

```bash
pip install -r requirements.txt
```

This is important for:

- reproducibility,
- collaboration,
- CI/CD,
- and deployment.

---

## 7. Create Initial Project Files

The initial project files were created:

```bash
touch README.md
touch .gitignore
touch pyproject.toml
touch .env.example
```

### `README.md`

The main documentation and entry point of the project.

It will later contain information such as:

- project purpose,
- architecture,
- technology stack,
- installation,
- and usage instructions.

### `.gitignore`

Defines files and directories that Git should not track.

Examples include:

```text
.venv/
__pycache__/
.env
```

This prevents local environments, temporary files, and secrets from being committed to the repository.

### `pyproject.toml`

Used for modern Python project and tool configuration.

It can later contain configuration for:

- project metadata,
- formatting,
- linting,
- testing,
- and other development tools.

### `.env.example`

Documents the environment variables required by the project without containing real secrets.

Example:

```text
DATABASE_USER=
DATABASE_PASSWORD=
```

The real `.env` file must not be committed to Git.

---

## 8. Project Management with Jira

Jira was selected for structured project planning and task tracking.

A Scrum-based project space was created.

**Space name:**

```text
Parvaneh Engineering
```

### Why Jira?

Jira provides practical project management functionality such as:

- backlog management,
- epics,
- tasks,
- priorities,
- sprints,
- and progress tracking.

Using Jira also makes the project development process closer to professional software and data engineering workflows.

---

## 9. Scrum Workflow

The project uses the following basic workflow:

```text
To Do → In Progress → Done
```

### To Do

The task has been planned but work has not started.

### In Progress

The task is currently being worked on.

### Done

The task has been completed.

---

## 10. Create the First Epic

The first Jira Epic was created:

```text
Project Foundation
```

**Jira ID:**

```text
SCRUM-1
```

**Description:**

```text
Establish the project foundation, define the business problem,
prepare the development environment and create the initial
project structure.
```

### Why use an Epic?

An Epic groups multiple related tasks that contribute to a larger project objective.

The `Project Foundation` Epic contains all work required to establish the technical and conceptual foundation of the project.

---

## 11. Create the Initial Backlog

Eight work items were created under the `Project Foundation` Epic.

### SCRUM-2 – Initialize GitHub Repository

Create and initialize the GitHub repository for version control and project collaboration.

### SCRUM-3 – Set Up Local Development Environment

Prepare the local Python development environment and install the initial dependencies.

### SCRUM-4 – Create Initial Project Structure

Create the initial directories and configuration files required for the project.

### SCRUM-5 – Write Business Case

Define the business problem, project motivation, stakeholders, and expected business value.

### SCRUM-6 – Define Functional Requirements

Define what the system must be able to do.

### SCRUM-7 – Define Non-Functional Requirements

Define quality requirements such as maintainability, security, performance, and reproducibility.

### SCRUM-8 – Design System Architecture

Design the high-level architecture and define how the different technologies and components interact.

### SCRUM-9 – Design Initial Data Model

Define the first version of the finance data model and the relationships between the main entities.

---

## 12. Jira Hierarchy

The current Jira structure is:

```text
Project
└── Epic: Project Foundation (SCRUM-1)
    ├── SCRUM-2: Initialize GitHub Repository
    ├── SCRUM-3: Set Up Local Development Environment
    ├── SCRUM-4: Create Initial Project Structure
    ├── SCRUM-5: Write Business Case
    ├── SCRUM-6: Define Functional Requirements
    ├── SCRUM-7: Define Non-Functional Requirements
    ├── SCRUM-8: Design System Architecture
    └── SCRUM-9: Design Initial Data Model
```

This separates the larger project objective from the individual implementation tasks.

---

## 13. Current Project Status

At the end of Day 1:

- the project idea was defined,
- the GitHub repository was created,
- the local Python environment was prepared,
- the initial dependencies were installed,
- the basic project files were created,
- Jira was configured,
- the first Epic was created,
- and the initial project backlog was prepared.

The next phase is to complete the remaining `Project Foundation` work items systematically.

---

## Key Learnings

### Virtual Environment

A Python virtual environment isolates project dependencies from the system Python installation.

### `requirements.txt`

Stores installed Python dependencies and their versions to make the environment reproducible.

### `.gitignore`

Prevents unnecessary files and sensitive information from being tracked by Git.

### GitHub

Manages source code and version history.

### Jira

Manages project planning and work progress.

### Epic

Represents a larger objective consisting of multiple related tasks.

### Backlog

Contains planned work that has not yet been completed.

### Sprint

Represents a defined period in which selected backlog items are worked on.

---

## Next Step

Continue with the `Project Foundation` Epic and complete the work items in a logical order, documenting each completed development step in this file.