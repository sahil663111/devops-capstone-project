# DevOps Capstone Project

[![CI Build](https://github.com/sahil663111/devops-capstone-project/actions/workflows/ci-build.yaml/badge.svg)](https://github.com/sahil663111/devops-capstone-project/actions/workflows/ci-build.yaml)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python 3.9](https://img.shields.io/badge/Python-3.9-green.svg)](https://shields.io/)

This repository contains the completed project for [**IBM-CD0285EN-SkillsNetwork DevOps Capstone Project**](https://www.coursera.org/learn/devops-capstone-project?specialization=devops-and-software-engineering) which is part of the [**IBM DevOps and Software Engineering Professional Certificate**](https://www.coursera.org/professional-certificates/devops-and-software-engineering).

## Project Overview

In this capstone project, you develop and manage a Customer Accounts microservice, applying key concepts of software development, automation, and cloud deployment:
- Defined user stories and organized sprints using GitHub Projects Kanban boards.
- Implemented RESTful APIs for CRUD operations (`CREATE`, `READ`, `UPDATE`, `DELETE`, and `LIST`).
- Followed Test-Driven Development (TDD) achieving high test coverage using `nosetests`.
- Configured Continuous Integration (CI) workflows with GitHub Actions.
- Added security features including Flask-Talisman security headers and CORS policies.
- Containerized the microservice using Docker.
- Deployed the containerized application to Kubernetes.
- Automated deployment via a Tekton Continuous Delivery (CD) pipeline.

## Project Layout

```text
├── service         <- microservice package
│   ├── common/     <- common log and error handlers
│   ├── config.py   <- Flask configuration object
│   ├── models.py   <- code for the persistent model
│   └── routes.py   <- code for the REST API routes
├── setup.cfg       <- tools setup config
└── tests           <- folder for all of the tests
    ├── factories.py            <- test factories
    ├── test_cli_commands.py    <- CLI tests
    ├── test_models.py          <- model unit tests
    └── test_routes.py          <- route unit tests
```

## Running the Service

```bash
gunicorn --bind=0.0.0.0:8080 --log-level=info service:app
```

## Running Tests and Linting

```bash
flake8 service tests
nosetests -v --with-spec --spec-color --with-coverage --cover-package=service
```

## Author

[sahil663111](https://github.com/sahil663111)

## License

Licensed under the Apache License, Version 2.0. See [LICENSE](LICENSE).
