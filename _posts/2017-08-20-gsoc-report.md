---
layout: post
title: Dockerization And New Instance setup
---

## Introduction

The Aim of the project was to replace the current VM stack which is being used to distribute the PEcAn with the Docker stack, Moreover develope interface to ease the user in the setup of the new Instance of the PEcAn. This is a short report on the project.

### Code Repository

I have worked on a fork of the [PEcAn](https://github.com/PecanProject/pecan.git) and can be found under my github profile [Amanskywalker/PEcAn](https://github.com/Amanskywalker/pecan.git)

### Milesontes (objectives)

1. **Dockerization** : Change the currently VM based distribution Into Docker Containers based distribution.

2. **New Instant Setup** :  Made a Admin page to have the functionalities like setup Unique machine id, Sync between the database, automatically update bety and PEcAn, Setup new instance etc.

## Work Report
The coding part of the project was done in 3 phases

#### Phase 1 :

**Dockerization** : In order to achieve the Dockerization, I have had to added new scripts like Dockerfile, Docker-composer, bash scripts to set up the Docker container. The Docker is logically divided into smaller containers like PEcAn-Core, PEcAn-web, Bety & PostgreSQL. They are communicating with each other to get the task accompleshed.

***Pull Request*** : The Pull Request for this phase can be found at  [github.com/PecanProject/pecan/pull/1485](https://github.com/PecanProject/pecan/pull/1485)

#### Phase 2 :

**Configuration Setup** : In order to design a configuration page, need to design a adaptive script which needed no or less modification to adapt to the changes in the corresponding config file. Also the 


[project link](https://summerofcode.withgoogle.com/projects/#5583766987735040)
