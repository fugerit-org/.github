# [Fugerit Coding Org](https://www.fugerit.org) - A development collection project

Version : 1.4.2, Date : 2024-02-10

*Introduction*  
The main purpose of this organization is to create simple libraries and tool for making development easier.

[![Keep a Changelog v1.1.0 badge](https://img.shields.io/badge/changelog-Keep%20a%20Changelog%20v1.1.0-%23E05735)](https://github.com/fugerit-org/.github/blob/main/profile/CHANGELOG.md) 
[![code of conduct](https://img.shields.io/badge/conduct-Contributor%20Covenant-purple.svg)](https://github.com/fugerit-org/fj-universe/blob/main/CODE_OF_CONDUCT.md)

*Index*
There are three main kind of projects hosted by [fugerit-org] github account
1. Core libraries 
2. Tools
3. Documentation and quickstarts

Most of them are maven projects, based on [fj-bom](https://github.com/fugerit-org/fj-bom) parent pom.  

In time some projects have been depcreated, here is the [list](http://github-org.fugerit.org/profile/DEPRECATED.html).

## 1. Core libraries

There are four main libraries, wchich are basically maven multi module projects : 
  
**1.0 [Bom (fj-bom)](https://github.com/fugerit-org/fj-bom)**
The parent pom with common resources and behaviours for other projects.  
[![Maven Central](https://img.shields.io/maven-central/v/org.fugerit.java/fj-bom.svg)](https://mvnrepository.com/artifact/org.fugerit.java/fj-bom)
[![license](https://img.shields.io/badge/License-Apache%20License%202.0-teal.svg)](https://opensource.org/licenses/Apache-2.0)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=fugerit-org_fj-bom&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=fugerit-org_fj-bom)

**1.1 [Jupiter (fj-lib)](https://github.com/fugerit-org/fj-lib)**  
This library contains a core libraries of functions covering many language primitives needed in project (configuration loading, IO, i18n ecc).  
With the exception of dbcp2, this library only depends on java 8 sdk.  
[![Maven Central](https://img.shields.io/maven-central/v/org.fugerit.java/fj-core.svg)](https://mvnrepository.com/artifact/org.fugerit.java/fj-core)
[![license](https://img.shields.io/badge/License-Apache%20License%202.0-teal.svg)](https://opensource.org/licenses/Apache-2.0)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=fugerit-org_fj-lib&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=fugerit-org_fj-lib)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=fugerit-org_fj-lib&metric=coverage)](https://sonarcloud.io/summary/new_code?id=fugerit-org_fj-lib) 

**1.2 [Venus (fj-doc)](https://github.com/fugerit-org/fj-doc)**  
This module defines a custom document module with some basic structures (paragraphs, tables, list etc.).  
In the core module there is the infrastructures for handling such documents.  
Submodules adds output fornmats thorough the used of third party libraries (i.e. Apache FOP for PDF or Apache POI for XLSX).  
NB: the submodules are divided as to optimize dependency injection when importing them.  
[![Maven Central](https://img.shields.io/maven-central/v/org.fugerit.java/fj-doc-base.svg)](https://mvnrepository.com/artifact/org.fugerit.java/fj-doc-base)
[![license](https://img.shields.io/badge/License-Apache%20License%202.0-teal.svg)](https://opensource.org/licenses/Apache-2.0)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=fugerit-org_fj-doc&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=fugerit-org_fj-doc)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=fugerit-org_fj-doc&metric=coverage)](https://sonarcloud.io/summary/new_code?id=fugerit-org_fj-doc) 

**1.3 [Mars (fj-daogen)](https://github.com/fugerit-org/fj-daogen)**
A code generation library, allowing for the creations of beans representing Entities and various functions to apply on them.
THe name daogen had been picked because simple persistence layer is provided, but it is possibile to add generator for different behaviours.  
[![Maven Central](https://img.shields.io/maven-central/v/org.fugerit.java/fj-daogen-base.svg)](https://mvnrepository.com/artifact/org.fugerit.java/fj-daogen-base)
[![license](https://img.shields.io/badge/License-Apache%20License%202.0-teal.svg)](https://opensource.org/licenses/Apache-2.0)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=fugerit-org_fj-daogen&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=fugerit-org_fj-daogen)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=fugerit-org_fj-daogen&metric=coverage)](https://sonarcloud.io/summary/new_code?id=fugerit-org_fj-daogen) 

**1.4 [Universe (fj-universe)](https://github.com/fugerit-org/fj-universe)**
A fugerit org universe bom project, still incubating, to handle of the dependencies at once!  
[![Maven Central](https://img.shields.io/maven-central/v/org.fugerit.java.universe/fj-universe.svg)](https://mvnrepository.com/artifact/org.fugerit.java.universe/fj-universe)
[![license](https://img.shields.io/badge/License-Apache%20License%202.0-teal.svg)](https://opensource.org/licenses/Apache-2.0)

## 2. Tools  

There are some specific tools for handling a few specific tasks : 

**2.1 [Native Helper GraalVM](https://github.com/fugerit-org/native-helper-graalvm)**
Helper tool to generate GraalVM native image metadata.
[![Maven Central](https://img.shields.io/maven-central/v/org.fugerit.java/native-helper-graalvm.svg)](https://mvnrepository.com/artifact/org.fugerit.java/native-helper-graalvm)
[![license](https://img.shields.io/badge/License-Apache%20License%202.0-teal.svg)](https://opensource.org/licenses/Apache-2.0)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=fugerit-org_native-helper-graalvm&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=fugerit-org_native-helper-graalvm)

**2.2 [Yaml Doc Tool](https://github.com/fugerit-org/yaml-doc-tool)**
This simple tool parses a yaml document and produces an output using the [Venus](https://github.com/fugerit-org/fj-doc) library. In the current version has been tested on yaml representing Openapi specification. A [maven plugin](https://github.com/fugerit-org/yaml-doc-maven-plugin) is also provided.  
[![Maven Central](https://img.shields.io/maven-central/v/org.fugerit.java/yaml-doc-tool.svg)](https://mvnrepository.com/artifact/org.fugerit.java/yaml-doc-tool)
[![license](https://img.shields.io/badge/License-Apache%20License%202.0-teal.svg)](https://opensource.org/licenses/Apache-2.0)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=fugerit-org_yaml-doc-tool&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=fugerit-org_yaml-doc-tool)

**2.3 [Query Export Tool](https://github.com/fugerit-org/query-export-tool)**  
Simple tool ti export query in CSV, HTML, XLS and XLSX formats.  
[![Maven Central](https://img.shields.io/maven-central/v/org.fugerit.java/query-export-tool.svg)](https://mvnrepository.com/artifact/org.fugerit.java/query-export-tool)
[![license](https://img.shields.io/badge/License-Apache%20License%202.0-teal.svg)](https://opensource.org/licenses/Apache-2.0)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=fugerit-org_query-export-tool&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=fugerit-org_query-export-tool)

**2.4 [Githib Issue Export](https://github.com/fugerit-org/github-issue-export)**  
Tool to export the list of issue in a github repository using the github api.  
[![Maven Central](https://img.shields.io/maven-central/v/org.fugerit.java/github-issue-export.svg)](https://mvnrepository.com/artifact/org.fugerit.java/github-issue-export)
[![license](https://img.shields.io/badge/License-Apache%20License%202.0-teal.svg)](https://opensource.org/licenses/Apache-2.0)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=fugerit-org_github-issue-export&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=fugerit-org_github-issue-export)

## 3. Documentation and quickstarts  

At last some repository are just documentation and samples to other projects. for instance :  

**3.1 [Venus Guides](https://github.com/fugerit-org/fj-doc-guides)**  
This project contains a quickstart for [Venus](https://github.com/fugerit-org/fj-doc) library. 
There is some documentation at [https://venusguides.fugerit.org/](https://venusguides.fugerit.org/)
and some specific purpose guide, like the classic [Hello World](https://github.com/fugerit-org/fj-doc-guides/tree/main/fj-doc-guides-A001-hello-world-pdf),

**3.2 [Venus Quickstart](https://github.com/fugerit-org/fj-doc-quickstart)**  
This project contains a quickstart for [Venus](https://github.com/fugerit-org/fj-doc) library. Many examples are provided including :  
* Static document
* Dynamic document (by use of freemarker)
* Code injection in rest application (springboot, websphere liberty and quarkus samples are provided)  


## 4. Credits

I would like to thanks the many projects (especially the open source one) which contributed so much to all the projects in those repository are built.  
All those projects are the building bricks which enable to create awesome software.  
It is not possible to invent every time the wheel from scratch, so none of the projects hosted by this organization would have ever existed without these building bricks.  
Here is a brief list of the main projects used by [Fugerit Coding Org Credits](http://github-org.fugerit.org/profile/credits.html)

## 5. Quality gate

See current [Sonar Cloud Quality Gate status](https://sonarcloud.io/organizations/fugerit-org/projects)

## 6. Other resources

* [release repository](https://repo1.maven.org/maven2/org/fugerit/java/)
* [snapshot repository](https://oss.sonatype.org/content/repositories/snapshots/org/fugerit/java/)

## Special thanks

**Special thanks** to [JetBrains](https://www.jetbrains.com/) 
for accepting this project in the 
[Licenses for Open Source Development - Community Support](https://jb.gg/OpenSourceSupport) program.

[![JetBrains](https://universe.fugerit.org/src/docs/thanks/jetbrains.png)](https://universe.fugerit.org/src/docs/thanks/jetbrains.html)

**Special thanks** to [Sonar Cloud](https://sonarcloud.io/), 
[Codacy](https://www.codacy.com/) and 
[Snyk](https://snyk.io/) 
too for their code review platforms.
