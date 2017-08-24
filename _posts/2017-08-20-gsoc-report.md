---
layout: post
title: Dockerization And New Instance setup
---

## Introduction

The Aim of the project is to replace the current VM stack which is being used to distribute the PEcAn with the Docker stack, Moreover develope interface to ease the user in the setup of the new Instance of the PEcAn. This is a short report on the [project](https://summerofcode.withgoogle.com/projects/#5583766987735040).

### Code Repository

I have worked on a fork of the [PEcAn](https://github.com/PecanProject/pecan.git) and can be found under my github profile [Amanskywalker/PEcAn](https://github.com/Amanskywalker/pecan.git)

### Milesontes (objectives)

1. **Dockerization** : Change the currently VM based distribution Into Docker Containers based distribution.

2. **New Instant Setup** :  Made a Admin page to have the functionalities like setup Unique machine id, Sync between the database, automatically update bety and PEcAn, Setup new instance etc.

## Work Report
The coding part of the project was done in 3 phases

#### Phase 1 :

**Dockerization** : In order to achieve the Dockerization, I have had to added new scripts like Dockerfile, Docker-composer, bash scripts to set up the Docker container. The Docker is logically divided into smaller containers like PEcAn-Core, PEcAn-web, Bety & PostgreSQL. They are communicating with each other to get the task accomplished.

The corresponding documentaion is updated so the user won't find it difficult to setup the docker containers.

***Pull Request*** : The Pull Request for this phase can be found at  [github.com/PecanProject/pecan/pull/1485](https://github.com/PecanProject/pecan/pull/1485)

#### Phase 2 :

**Configuration Setup** : In order to design a configuration page, needed to design a adaptive script which need no or less modification to adapt to the changes in the corresponding config file. Also the design aspect include the frameworks like bootstrap which made the page responsive.
A brief description of the use of the setup page is added in the documentaion.

***Pull Request*** : The Pull Request for this phase can be found at  [github.com/PecanProject/pecan/pull/1541](https://github.com/PecanProject/pecan/pull/1541)

#### Phase 3 :

**Syncronization** : In this phase the objective was to setup the syncronization of database between two system, the request response cycle use the JSON to communicate with each other. Also a cron job is made which runs in the backgroud to make sure the syncronization is done. Further the registration and genration of the tokes are automated so it don't need user intervantion.
A new submit bug page is maded as post bug report from within the application.

***Pull Request*** : The Pull Request for this phase can be found at  [github.com/PecanProject/pecan/pull/1589](https://github.com/PecanProject/pecan/pull/1589)

## Conclusion

Most of the part which are metioned in the proposal are done, few small things were left out like feedback page, Automatic update whenever a new version is released etc.

Further there are few new things which can be done to extent this work
- In setup page provision to add new host in config.php page further to edit existing host.
- Give user power to chose the host to sync with to be passed in dump.bety.sh, default being all.
- Seperating the model from the PEcAn-Core and making them independent and can be communicated via netowrks to use it.
- Using the above way to spin the models as required to enable parallel execution in PEcAn.
