---
title: What is multi-repository
---


The multi-repo approach uses several repositories to host the multiple libraries or services of a project. At its most extreme, it will host every minimum set of reusable code or standalone functionality (such as a microservice) under its own repository.

## Advantages of Multi-repo

- Each service and library have its own versioning
- Code check-outs and pulls are small and separate, thus there are no performance issues even if the project size grows
- Teams can work independently and do not need access to the entire codebase
- Faster development and flexibility
- Each service can be released separately and have its own deployment cycle
- Better access control – all teams do not need to have full access to all the libraries – but can get read access if they need

### Independent library versioning

When tagging a repository, its whole codebase is assigned the “new” tag. Since only the code for a specific library is on the repository, the library can be tagged and versioned independently of all other libraries hosted elsewhere.

Having an independent version for every library helps define the dependency tree for the application, allowing us to configure what version of each library to use.

### Independent service releases

Since the repository only contains the code for some service and nothing else, it can have its own deployment cycle, independently of any progress made on the applications accessing it.

The service can use a fast release cycle such as continuous delivery (where new code is deployed after it passes all the tests). Some libraries accessing the service may use a slower release cycle.

### Helps define access control across the organization

Only the team members involved with developing a library need to be added to the corresponding repository and download its code. As a result, there’s an implicit access control strategy for each layer in the application. Those involved with the library will be granted editing rights, and everyone else may get no access to the repository. Or they may be given reading rights only.

### Allows teams to work autonomously

Team members can design the library’s architecture and implement its code working in isolation from all other teams. They can make decisions based on what the library does in the general context without being affected by the specific requirements from some external team or application.

## Disadvantages of multi-repo

- Dependencies and libraries used across services and projects have to be regularly synced to get the latest version
- Encourages a siloed culture, leading to duplicate code and individual teams trying to resolve the same problem
- Each team may follow a different set of best practices for their code causing difficulties in following common best practices
- Heavier workload on CI/CD and tests development since they are separated for each service.

### Libraries must constantly be resynced

When a new version of a library containing breaking changes is released, libraries depending on this library will need to be adapted to start using the latest version. If the release cycle of the library is faster than that of its dependent libraries, they could quickly become out of sync with each other.

Teams will need to constantly catch up to use the latest releases from other teams. Given that different teams have different priorities, this may sometimes prove arduous to achieve.

Consequently, a team not able to catch up may end up sticking to the outdated version of the depended-upon library. This outcome will have implications on the application in terms of security and speed, and the gap in development across libraries may only get wider.

### May fragment teams

When different teams do not need to interact, they may work in their own silos. In the long term, this could result in teams producing their subcultures within the company, such as employing different methodologies of programming or management or using different sets of development tools.

If some team member eventually needs to work in a different team, they may suffer a bit of culture shock and need to learn a new way of doing their job.

### More devops tasks

Some members of the team will need to maintain a more complex CI/CD pipeline and tests. In order to properly handle the benefits of a multi-repo approch such as faster development and delivery.
