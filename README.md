
# DevOps Capstone Project

![Build Status](https://github.com/nadine-elsayed/devops-capstone-project/actions/workflows/ci-build.yaml/badge.svg)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python 3.9](https://img.shields.io/badge/Python-3.9-green.svg)](https://shields.io/)

This repository contains my project for the [**IBM-CD0285EN-SkillsNetwork DevOps Capstone Project**](https://www.coursera.org/learn/devops-capstone-project?specialization=devops-and-software-engineering), part of the [**IBM DevOps and Software Engineering Professional Certificate**](https://www.coursera.org/professional-certificates/devops-and-software-engineering).

---

## 📌 Project Overview

In this Capstone project, I applied the technologies and concepts I learned throughout the IBM DevOps program to build a **Customer Accounts microservice**.

- **Module 1**: I started by planning the project using Agile practices. I created a GitHub repository, built a Kanban board, and added a user story template. I then populated the backlog with user stories, estimated story points, and organized everything into a sprint backlog.
  
- **Module 2**: I began Sprint 1 by configuring the environment and developing the microservice using **Test-Driven Development (TDD)**. I created test cases for the `READ`, `UPDATE`, `DELETE`, and `LIST` functionalities and implemented enough code for all tests to pass using `nosetests` and `coverage`.

- **Module 3**: I configured a **GitHub Actions CI pipeline** to automatically run on pull requests or pushes to the main branch. The workflow runs tests, checks code quality with Flake8, and ensures 95%+ coverage using `coverage`.

- I added security enhancements like **Flask-Talisman** for secure headers and **Flask-CORS** to manage cross-origin policies, and I followed TDD by writing tests for these features before implementation.

- **Module 4**: In Sprint 3, I containerized the microservice using **Docker** and deployed it manually to an **OpenShift/Kubernetes** cluster using YAML manifests. I also created a **PostgreSQL service** as the backend database.

- Finally, I automated the entire CI/CD flow using a **Tekton pipeline** that builds, tests, and deploys the service automatically when triggered.

## 🧱 Local Setup (Optional)

To simulate the Cloud IDE locally:

### ✅ Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop)
- [VS Code](https://code.visualstudio.com) + [Remote Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

### ⚙️ Quick Setup

1. Start a local K3D Kubernetes cluster:

    ```bash
    make cluster
    ```

2. Install Tekton:

    ```bash
    make tekton
    ```

3. Add Cloud IDE ClusterTasks:

    ```bash
    make clustertasks
    ```
    
## 🚀 Run Locally

1. **Clone the repo** and navigate into it:

   ```bash
   git clone https://github.com/nadine-elsayed/devops-capstone-project.git
   cd devops-capstone-project
   ```

2. **Set up the virtual environment:**

   ```bash
   python3.9 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies:**

   ```bash
   make install
   ```

4. **Start the PostgreSQL database (Docker required):**

   ```bash
   make db
   ```

5. **Run the app:**

   ```bash
   flask run
   ```

6. **Verify it's running:** Open `http://localhost:5000` in your browser.

## 📝 License

Licensed under the Apache License. See [LICENSE](LICENSE) for more information.

---

<h3 align="center">© IBM Corporation 2022. All rights reserved.</h3>
