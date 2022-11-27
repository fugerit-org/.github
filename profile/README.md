# [Fugerit Coding Org](https://www.fugerit.org) - A development collection project

Version : 0.0.1, Date : 2022-11-27

*Introduction*  
The main purpose of this organization is to create simple libraries and tool for making development easier.

*Index*
There are three main kind of projects hosted by [fugerit-org] github account
1. Core libraries 
2. Tools
3. Documentation and quickstarts

Most of them are maven projects, based on [fj-bom](https://github.com/fugerit-org/fj-bom) parent pom.  

In time some projects have been depcreated, here is the [list](DEPRECATED.md).

## 1. Core libraries

There are thre main libraries, wchich are basically maven multi module projects : 

**1.1 [Jupiter (fj-lib)](https://github.com/fugerit-org/fj-doc)**  
This library contains a core libraries of functions covering many language primitives needed in project (configuration loading, IO, i18n ecc).  
With the exception of dbcp2, this library only depends on java 8 sdk.

**1.2 [Venus (fj-doc)](https://github.com/fugerit-org/fj-doc)**  
This module defines a custom document module with some basic structures (paragraphs, tables, list etc.).  
In the core module there is the infrastructures for handling such documents.  
Submodules adds output fornmats thorough the used of third party libraries (i.e. Apache FOP for PDF or Apache POI for XLSX).  
NB: the submodules are divided as to optimize dependency injection when importing them.  

**1.3 [Mars (fj-daogen)](https://github.com/fugerit-org/fj-daogen)**
At last this is basically a code generation library, allowing for the creations of beans representing Entities and various functions to apply on them.
THe name daogen had been picked because simple persistance layer is provided, but it is possibile to add generator for different behaviours. 


## 2. Tools  

There are some specific tools for handling a few specific tasks : 

**2.1 [Freemarker Maven Plugin](https://github.com/fugerit-org/freemarker-maven-plugin)**
This is our versions of freemarker maven plugin. Originally a fork of the original [repository](https://github.com/yahoo/freemarker-maven-plugin) hosted by [yahoo](https://github.com/yahoo) account. This plugin simply allow to handle freemarker templates during the maven build process.


**2.2 [Yaml Doc Tool](https://github.com/fugerit-org/yaml-doc-tool)**
This simple tool parses a yaml document and produces an output using the [Venus](https://github.com/fugerit-org/fj-doc) library. In the current version has been tested on yaml representing Openapi specification. A [maven plugin](https://github.com/fugerit-org/yaml-doc-maven-plugin) is also provided.


## 3. Documentation and quickstarts  

At last some repository are just documentation and samples to other projects. for instance :  

**3.1 [Venus Quickstart](https://github.com/fugerit-org/fj-doc-quickstart)**  
This project contains a quickstart for [Venus](https://github.com/fugerit-org/fj-doc) library. Many examples are provided including :  
* Static document
* Dynamic document (by use of freemarker)
* Code injection in rest application (springboot, websphere liberty and quarkus samples are provided)  