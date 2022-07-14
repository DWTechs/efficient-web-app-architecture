---
title: Conclusion
---

## How to choose?

Different companies and projects will benefit from one strategy or the other based on their unique conditions.
Here is a list of criterias you can use to help you choose : 

- Are different programming languages involved? Do they require a particular software installed or special hardware to run? 
- How many deployment tools are required, and how complex are they to set up?
- What is the culture in the company? Are teams encouraged to collaborate or work independently?
- How big is the codebase?
- How many people will work on the codebase?
- How many packages (or services) will there be?
- How many packages does the team need to work on at a given time?
- How tightly coupled are the packages?

## Summary

Both mono-repo and multi-repo are equally popular and the choice depends on your project size, requirements, and the level of versioning and access control you need.

Mono-repo favors consistency, whereas multi-repo focuses on decoupling. 

Multi-repo will favor faster development and delivery (if teams are organized accordingly) but will need more care on the CI/CD side.
So ultimately you need to decide at which project/teams size adding those devops tasks is less expensive than the benefits 

**Given our structure and the size of projects we usually develop, we favor a mono-repo strategy (at the application level) as it facilitates team coordination and workflows.**
