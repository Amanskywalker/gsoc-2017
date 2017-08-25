---
layout: post
title: Dockerization And New Instance setup
---

## Introduction

Aim of this project is to replace the current VM stack which is being used to distribute the PEcAn with Docker stack, moreover develop the existing interface to ease the user in the setup of new instance of PEcAn. Here's a short report on the [project](https://summerofcode.withgoogle.com/projects/#5583766987735040).

### Code Repository

I have worked on a fork of [PEcAn](https://github.com/PecanProject/pecan.git) and the changes are under my github profile [Amanskywalker/PEcAn](https://github.com/Amanskywalker/pecan.git)

### Milestones ( Objectives )

1. **Dockerization** : Change the currently used VM based distribution into Docker container based distribution.

2. **New Instant Setup** :  Made an admin page to have the functionalities like setup unique machine ID, sync between the databases, automatically update BETY and PEcAn and setup new instance etc.

## Work Report
The coding part of the project was carried out in 3 phases

#### Phase 1 :

**Dockerization** : In order to achieve Dockerization, I have added new scripts like Dockerfile, Docker-composer, bash scripts to set up Docker containers. It is logically divided into smaller containers like PEcAn-Core, PEcAn-web, BETY & PostgreSQL. They are able to communicate with each in order to accomplish tasks.

The corresponding documentation is updated so the user won't find it difficult to setup Docker containers.

***Pull Request*** : Pull request for this phase can be found at  [github.com/PecanProject/pecan/pull/1485](https://github.com/PecanProject/pecan/pull/1485)

#### Phase 2 :

**Configuration Setup** : To design a configuration page, it was required to design an adaptive script which needed few or no modifications to adapt the changes in the corresponding config file. Also the design aspects include frameworks like bootstrap which made the page responsive.

A brief description on use of the setup page is added in the documentation.

***Pull Request*** : Pull request for this phase can be found at  [github.com/PecanProject/pecan/pull/1541](https://github.com/PecanProject/pecan/pull/1541)

#### Phase 3 :

**Synchronization** : Here the objective was to setup synchronization of databases between two systems/machines, the request-response-cycle uses JSON to communicate with each other. Also Cron-job is added which runs in the background to make sure that synchronization is performed. Further registration and generation of tokens are automated so that it doesn't requires any user intervention.

A new bug reporting mechanism is added within the application to automate it.

***Pull Request*** : Pull request for this phase can be found at  [github.com/PecanProject/pecan/pull/1589](https://github.com/PecanProject/pecan/pull/1589)

## Conclusion

Most of which mentioned in the proposal is done, few small concerns which are left out are feedback page and automatic updatation whenever a new version is released.

Further, here are a few notable changes which can be done to extend this work
- In the setup page, a provision can be made to add new host in config.php page, further to edit existing host.
- Give user power to choose the host to sync, default being all.
- Seperating the model from the PEcAn-Core and making them independent containers.
- Using the above model, create a way to spin and use the models as required to enable parallel execution in PEcAn.
