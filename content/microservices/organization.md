---
title: Organization
---

## Managing microservices in a mono-repo strategy

Microservices architecture implies thorough reflection on the way of working and organization of the teams.
With Docker-compose and Gitlab CI we optimize processes and ensure Microservices architecture and mono-repo strategy are used at their full potential by fully facilitate workflows and team work. 

Those tools helps the teams deliver efficiently and undertake inherent challenges of this architecture :   

- Integration: Manage relations between all microservices "natively" within one repository
- Versioning: Secure the global version and history with proper package management
- Environment setup: Pull and launch the application in few minutes with Docker-compose
- CI/CD: Test and deploy the application autmaticaly with low maintenance cost with Docker and Gitlab CI.

## Git

When making changes to a service, it is important to make sure the rest of the application will follow. Meaning each member must have a good global knowledge of the application and what may break on the other side of the application after the current changes are made.

## Docker

Docker is a set of platform as a service (PaaS) products that use OS-level virtualization to deliver software in packages called containers.
It can package each service of an application and its dependencies in its own virtual container that can run in local environment, on-premises or in the cloud.

### Docker Compose

Docker Compose is a tool for defining and running multi-container Docker applications.
It uses YAML files to configure the application's services and performs the creation and start-up process of all the containers with a single command.
The docker-compose CLI utility allows users to run commands on multiple containers at once, for example, building images, scaling containers, running containers that were stopped, and more.
The docker-compose.yml file is used to define an application's services and includes various configuration options.


## Gitlab CI

GitLab CI is used for all of the continuous Integration and Deployment. With GitLab CI, we can test, build, and publish the software with no third-party application.


