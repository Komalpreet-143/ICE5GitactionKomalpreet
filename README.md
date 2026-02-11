# GitHub Actions Lab

## Overview

This repository demonstrates two GitHub Actions workflows:

1. Dependent Jobs Workflow
2. Multi-Platform Testing Workflow

---

## Workflow 1: Dependent Jobs

### Purpose
This workflow demonstrates job dependencies using the `needs` keyword.

### Key Concepts Demonstrated

- `needs` → Controls execution order between jobs
- `runs-on` → Specifies the operating system for a job
- Multiple steps within jobs
- Sequential job execution

### Execution Order

build → test → deploy

Each job waits for the previous job to complete successfully before starting.

---

## Workflow 2: Multi-Platform Testing

### Purpose
This workflow demonstrates parallel execution of independent jobs across multiple operating systems.

### Key Concepts Demonstrated

- Parallel jobs (no `needs`)
- Running jobs on different OS platforms:
  - Ubuntu
  - Windows
  - macOS
- Using `actions/checkout@v4`
- OS-specific commands

All three jobs run simultaneously when a pull request is created.

---

## Challenges Faced

- Ensuring correct YAML indentation
- Using OS-specific commands for Windows vs Linux/macOS
- Making sure workflows triggered on the correct events

These were resolved by validating YAML syntax and reviewing workflow logs in the Actions tab.
