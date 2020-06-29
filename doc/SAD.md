# KeyCloud  - Software Architecture Document

## Table of Contents
- [KeyCloud  - Software Architecture Document](#keycloud---software-architecture-document)
  - [Table of Contents](#table-of-contents)
  - [1. Introduction](#1-introduction)
    - [1.1 Purpose](#11-purpose)
    - [1.2 Scope](#12-scope)
    - [1.3 Definitions, Acronyms and Abbreviations](#13-definitions-acronyms-and-abbreviations)
    - [1.4 References](#14-references)
    - [1.5 Overview](#15-overview)
  - [2. Architectural Representation](#2-architectural-representation)
    - [2.1 Technologies used](#21-technologies-used)
  - [3. Architectural Goals and Constraints](#3-architectural-goals-and-constraints)
  - [4. Use-Case View](#4-use-case-view)
    - [4.1 Use-Case Realizations](#41-use-case-realizations)
  - [5. Logical View](#5-logical-view)
    - [5.1 Design Pattern](#51-design-pattern)
  - [6. Process View](#6-process-view)
  - [7. Deployment View](#7-deployment-view)
  - [8. Implementation View](#8-implementation-view)
    - [8.1 Overview](#81-overview)
    - [8.2 Layers](#82-layers)
  - [9. Data View](#9-data-view)
  - [10. Size and Performance](#10-size-and-performance)
  - [11. Quality](#11-quality)

## 1. Introduction
### 1.1 Purpose
This document provides an architectural overview of the system, using a number of different architectural views.
### 1.2 Scope
The scope of this SAD is to show the overall architecture of the KeyCloud project. Use-Cases, classes used in the backend and the database structure are depicted.
### 1.3 Definitions, Acronyms and Abbreviations
Abbreviation | |
--- | --- 
IDE | Integrated Development Environment
MVC | Model View Controller
n/a | not applicable  
SAD | Software Architecture Document
SRS | Software Requirements Specification
tbd | to be determined
UC | Use Case

Definition | |  
--- | ---  
Software Architecture Document | The Software Architecture Document provides a comprehensive architectural overview of the system, using a number of different architectural views to depict different aspects of the system.
### 1.4 References
Title | Date | Publishing organization |  
--- | :---:  | ---
[KeyCloud Blog](https://keycloud.zeekay.dev/) | 12.10.2019 | KeyCloud  
[YouTrack Instance](https://youtrack.zeekay.dev/) | 12.10.2019 | KeyCloud  
[SRS](../doc/SRS.md) | 12.10.2019 | KeyCloud  
[TeamCity](https://teamcity.zeekay.dev/) | 19.11.2019 | KeyCloud
[KeyCloud Application](https://keycloud-dev.zeekay.dev/dashboard/) | 27.06.2020 | KeyCloud
### 1.5 Overview
This document contains the architectural representation, goals and constraints.

## 2. Architectural Representation
Our application is build using Golang in the backend and Angular (cosmetics are made using material design). 
Because Golang is a multi-paradigm language which mainly works functional, we do not have relationships between our classes. 
This is also the reason why we don't have a MVC architecture. Nevertheless, we tried our best to divide our classes up in these three categories.
### 2.1 Technologies used
IDEs:
- Frontend: JetBrains WebStorm
- Backend: JetBrains GoLand

Languages:
- Frontend: 
- Backend: Golang
- Database: PostgreSQL
- Testing: Java (Cucumber), Golang, Karma test, User test

## 3. Architectural Goals and Constraints
n/a

## 4. Use-Case View
![Use Case Diagram](img/UseCases.png)
### 4.1 Use-Case Realizations
tbd

## 5. Logical View
The following graphic describes the overall class organization of the backend.  
![Class-Diagram](./backend/ClassDiagram.PNG)
### 5.1 Design Pattern
The adapter design pattern is contained with the usage of the StorageInterface (upper-left corner). It enables us to completly isolate the way we store our data, from the way we consume it, as the interface is only defined by the interface. This allowed to simplify development at the beginning by simply use a dummy in-memory way of storing the actual data. Later on within the development we were able to connect a database by writing new functions that implement the StorageInterface without changing a single line of code of our logic part. Even in the future we can just add new ways of storing the data, only by adding a new implementation of the interface.
## 6. Process View
n/a

## 7. Deployment View  
![Deployment View](img/DeploymentView.png)

## 8. Implementation View
n/a
### 8.1 Overview
n/a
### 8.2 Layers
n/a

## 9. Data View
The following diagram describes the relationship model of our database.  
![Entity-Relation Diagram](backend/database/er-diagram.png)

## 10. Size and Performance
tbd

## 11. Quality
tbd
