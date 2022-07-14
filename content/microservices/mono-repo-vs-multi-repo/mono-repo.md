---
title: What is Mono-repository
---

The mono-repo approach uses a single repository to host all the code for the multiple services composing a micro-services.
At its most extreme, the whole codebase from a company — spanning various projects and coded in different languages — can be hosted in a single repository but here we will only talk about one micro-services application.

## Advantages of Mono-repo

- A single place to store all the project code. Can be accessed by everyone in the team
- Easy to reuse and share code, collaborate with teams
- Easy to understand the impact of your change on the entire project. Team members can get an overall view of the entire project
- Great for code-refactoring and large changes to code
- Easy to manage dependencies
- Light workload on CI/CD development and test runs since their are global to the entire application.

### Lowers barriers of entry

When new staff members start working for a company, they need to download the code and install the required tools to begin working on their tasks. Suppose the project is scattered across many repositories, each having its installation instructions and tooling required. Even if there are tools to automate this, it is still more compicated to understand and use. Plus someone had to write these automation at some point and still has to maintain it. There is a great chance that the documentation will not be complete anymore, requiring these new team members to reach out to colleagues for help.

A monorepo simplifies workflow to start a project. Since there is a single location containing all code and documentation, you can streamline the initial setup.

### Centrally located code management

Having a single repository gives visibility of all the code to all developers. It simplifies code management since we can use a single issue tracker to watch all issues throughout the application’s life cycle.

For instance, these characteristics are valuable when an issue spans two (or more) child libraries with the bug existing on the dependent library. With multiple repositories, it may be challenging to find the piece of code where the problem happens.

On top of this, we would need to figure out which repository to use to create the issue and then invite and cross-tag members of other teams to help resolve the problem.

With a monorepo, both locating code problems and collaborating to troubleshoot become simpler to achieve.

### Easier application-wide refactoring

When creating an application-wide refactoring of the code, multiple libraries will be affected. If you’re hosting them via multiple repositories, managing all the different pull requests to keep them synchronized with each other can be a challenge.

A monorepo makes it easy to perform all modifications to all code for all libraries and submit it under a single pull request.

### Uniform development culture

Since they will share the same repository, Teams will most likely share the same programming and management methodologies and use the same development tools.


## Issues of mono-repo

- Performance. If your project grows and more files are added everyday, the check-out, pull and other operations might become slow and file searches may take longer.

- If you hire a lot of independent contractors for your project, giving them access to the entire code base may not be so secure.

- Large companies that use mono-repos had to create customized tools to handle some scaling-up issues.

### Slower development cycles

When the code for a library contains breaking changes, which make the tests for dependent libraries fail, the code must also be fixed before merging the changes.

If these libraries depend on other teams and they are busy working on some other task the development of the new feature may stall.

The project may well start advancing at the speed of the slowest team in the company. This outcome could frustrate the members of the fastest teams.

This is not the case for a multi-repo application where each service is independant and will have several versions to work with other services wether they are up to date or not.

In addition, a library will need to run the tests for all other libraries too. The more tests to run, the more time it takes to run them, slowing down how fast we can iterate on our code.

### Requires download of entire codebase

When the mono-repo contains all the code for the application, it can be huge, containing gigabytes of data. To contribute to any library hosted within, anybody would require a download of the whole repository.

Dealing with a vast codebase implies a poor use of space on your hard drives and slower interactions with it. For instance, everyday actions such as executing git status or searching in the codebase with a regex may take many seconds or even minutes longer than they would with multiple repos.

### Unmodified libraries may be newly versioned

When we tag the mono-repo, all code within is assigned the new tag. If this action triggers a new release, then all libraries hosted in the repository will be newly released with the version number from the tag, even though many of those libraries may not have had any change.

### Forking is more difficult

Open source projects must make it as easy as possible for contributors to become involved. With multiple repositories, contributors can head directly to the specific repository for the project they want to contribute to. With a mono-repo hosting various projects, though, contributors must first navigate their way into the right service and will need to understand how their contribution may affect all other services.

