## Table of Contents
- [Table of Contents](#table-of-contents)
- [1. Use-Case Create Account](#1-use-case-create-account)
  - [1.1 Brief Description](#11-brief-description)
- [2. Flow of Events](#2-flow-of-events)
  - [2.1 Basic Flow](#21-basic-flow)
    - [2.1.1 Activity Diagram](#211-activity-diagram)
    - [2.1.2 Mock up](#212-mock-up)
      - [Register](#register)
      - [Create Password](#create-password)
  - [2.2 Alternative Flows](#22-alternative-flows)
- [3. Special Requirements](#3-special-requirements)
- [4. Preconditions](#4-preconditions)
- [5. Postconditions](#5-postconditions)
- [6. Extension Points](#6-extension-points)
- [7. Function Points](#7-function-points)

## 1. Use-Case Create Account
### 1.1 Brief Description
This use case allows the user to create an account. For the creation following credentials must be provided:
- username

## 2. Flow of Events
### 2.1 Basic Flow
- User enters username
- User clicks on register
- User is prompted with a password
#### 2.1.1 Activity Diagram
![UC_CreateAccount](img/UC/UC_CreateAccount.png) 
 
.feature  
![FeatureFile](img/featureFileScreenshots/Featurefile_UC_RegisterAccount.PNG)
#### 2.1.2 Mock up
##### Register
![Mockup_Register](img/mockups/Mockup_register.PNG)
##### Create Password
![Mockup_CreatePassword](img/mockups/Mockup_createPassword.PNG)
### 2.2 Alternative Flows
n/a

## 3. Special Requirements
n/a

## 4. Preconditions
n/a

## 5. Postconditions
If a user completes this workflow, the users profile must have been created on the server. 

## 6. Extension Points
n/a

## 7. Function Points
![FP_CreateAccount](img/UC/functionPoints/createAccount.jpg)