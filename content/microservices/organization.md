---
title: Organization
---

## Managing microservices in a multi-repo strategy

Microservices architecture implies thorough reflection on the way of working and organization of the teams.
With git submodules, Docker-compose and Gitlab CI we optimize processes and ensure Microservices architecture and multi-repo strategy are used at their full potential by fully decoupling services. 

Those tools helps the teams deliver efficiently and undertake inherent challenges of this architecture :   

- Integration: Manage relations between all microservices with Git submodules
- Versioning: Secure the global version and history with separated services with Git submodules
- Environment setup: Launch the application in few minutes with Git submodules and Docker
- CI/CD: Test and deploy the application autmaticaly with low maintenance cost with Docker and Gitlab CI.


## Git submodules

Git submodules are a powerful way to leverage git as an external dependency management tool. 
They keep git repositories as subdirectories of a main git repository.
A submodule is a reference to another repository at a particular snapshot in time.
They enable a Git repository to incorporate and track version history of external code.
It maintains a strict version management over external dependencies.

### Workflow

Once submodules are initialized within a parent repository they can be used like stand-alone repositories. They have their own branches and history. 
So when making changes to a submodule it is important to publish submodule changes and then update the parent repositories reference to the submodule.

Executing git status on parent level shows the parent repository is aware of the new commits to the service submodule.
Now you need to update the parent repository by doing a git add and git commit on the submodule. This will put everything into a good state with the local content.
Since you are working in a team environment it is critical that you then git push the submodule updates, and the parent repository updates.


## Docker

Docker is a set of platform as a service (PaaS) products that use OS-level virtualization to deliver software in packages called containers.
It can package an application and its dependencies in a virtual container that can run in local environment, on-premises or in the cloud.

### Docker Compose

Docker Compose is a tool for defining and running multi-container Docker applications.
It uses YAML files to configure the application's services and performs the creation and start-up process of all the containers with a single command.
The docker-compose CLI utility allows users to run commands on multiple containers at once, for example, building images, scaling containers, running containers that were stopped, and more.
The docker-compose.yml file is used to define an application's services and includes various configuration options.


## Gitlab CI

GitLab CI is used for all of the continuous Integration and Deployment. With GitLab CI, we can test, build, and publish the software with no third-party application.


