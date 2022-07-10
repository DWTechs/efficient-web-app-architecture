---
title: Conclusion
---

## How to choose?

Different companies and projects will benefit from one strategy or the other based on their unique conditions.
Here is a list of criteria you can use to help you chose : 

- Are different programming languages involved? Do they require a particular software installed or special hardware to run? Mono if only one language. Multi if several
- How many deployment tools are required, and how complex are they to set up? Mono if only one tool. Multi if several
- What is the culture in the company? Are teams encouraged to collaborate or work independently ?
- How big is the codebase? Mono for smaller ones, multi for biggest ones
- How many people will work on the codebase? Mono for smaller ones, multi for biggest ones
- How many packages will there be? The answer for this question dependents of the other questions.
- How many packages does the team need to work on at a given time? Multi for smaller ones, mono for biggest ones
- How tightly coupled are the packages? Mono if tightly coupled, multi otherwise

## Summary

Both mono-repo and multi-repo are equally popular and the choice depends on your project size, project requirements, and the level of versioning and access control you need.

Mono-repo favors consistency, whereas multi-repo focuses on decoupling. 

Multi repo will favor faster development and delivery on one hand but will need more care on the CI/CD side.
So ultimately you need to decide at which project/teams size adding those devops tasks is less expensive than the benefits of faster development.
