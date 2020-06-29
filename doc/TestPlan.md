# Test plan

## 1. Introduction
### 1.1	Purpose
The purpose of the Iteration Test Plan is to gather all of the information necessary to plan and control the test effort for a given iteration. 
It describes the approach to testing the software.
This Test Plan for **KeyCloud** supports the following objectives:
-	Identifies the motivation for and ideas behind the test areas to be covered.
-	Outlines the testing approach that will be used.
-	Identifies the required resources and provides an estimate of the test efforts.

### 1.2	Scope
This document describes the used tests, as they are unit tests and functionality testing.

### 1.3	Intended Audience
This document is meant to provide a coherent overview of the testing conducted in the KeyCloud organization.

### 1.4	Document Terminology and Acronyms
- **SRS**	Software Requirements Specification
- **n/a**	not applicable
- **tbd**	to be determined

### 1.5	 References
| Reference        | 
| ------------- |
| [SAD](SAD.md) | 
| [SRS](SRS.md) | 

            
## 2. Evaluation Mission and Test Motivation
### 2.1	Background
By testing source code, we ensure our application to run smoothly. The goal is to make sure, that our application does not run into any unexpected errors.
### 2.2	Evaluation Mission
The mission of this test plan is to prevent errors in production and ensure an outstanding software quality.
### 2.3	Test Motivators
Our testing is motivated by 
- quality risks 
- technical risks,
- functional requirements

## 3. Target Test Items
The listing below identifies those test items (software, hardware, and supporting product elements) that have been identified as targets for testing. 
This list represents what items will be tested. 

Items for Testing:
- KeyCloud Backend (Golang)
- KeyCloud Frontend (Angular / TS)

## 4. Outline of Planned Tests
### 4.1	Outline of Test Inclusions
Unit Testing for the backend.  
Behaviour Driven Testing for the Frontend.  
### 4.2	Outline of Other Candidates for Potential Inclusion
Simulating cyber attacks onto the server.
### 4.3 Outline of Test Exclusions
Unit Testing in the frontend is currently not part of the planned strategy.

## 5. Test Approach
### 5.1 Initital Test-Idea Catalogs and Other Reference Sources
**n/a**
### 5.2	Testing Techniques and Types
#### 5.2.1 KeyCloud Backend Testing (Unit Testing)
|||
|---|---|
|Technique Objective  	| Several functions in the backend will be called, their results will be compared with predefined results |
|Technique 		| Data should be mocked. Backend will not be started, no datastore will be used |
|Oracles 		| Functions return the correct and expected data. |
|Required Tools 	| Golang testing package |
|Success Criteria	| expected responses, passing tests |
|Special Considerations	|     -          |


#### 5.2.1 KeyCloud Frontend Testing (Behaviour Driven Testing)
|| |
|---|---|
|Technique Objective  	| Interactions defined in the tests should behave as expected |
|Technique 		|  Data should be mocked. |
|Oracles 		| Application behaves as expected. |
|Required Tools 	| Jasmine test framework, Angular, TS |
|Success Criteria	| expected responses, passing tests |
|Special Considerations	|     -          |

#### 5.2.2 Business Cycle Testing
**n/a**

#### 5.2.3 User Interface Testing
User interface testing done by an external user group, results are gathered through a questionaire, more information can be found [here](https://keycloud.zeekay.dev/2020/06/28/week-19-user-test/).

#### 5.2.4 Performance Profiling 
**n/a**

#### 5.2.5 Load Testing
**n/a**

#### 5.2.6 Stress Testing
**n/a**

#### 5.2.7	Volume Testing
**n/a**

#### 5.2.8	Security and Access Control Testing
**n/a**

#### 5.2.9	Failover and Recovery Testing
**n/a**

#### 5.2.10	Configuration Testing
**n/a**

#### 5.2.11	Installation Testing
Test installation done by an external user group, more information can be found [here](https://keycloud.zeekay.dev/2020/06/20/week-18-installation/#comment-115).

## 6. Entry and Exit Criteria
### 6.1	Test Plan
#### 6.1.1	Test Plan Entry Criteria
A series of build steps is executed in Teamcity. The tests are run within these build steps
#### 6.1.2	Test Plan Exit Criteria
When all tests pass without throwing an exception.
#### 6.1.3 Suspension and Resumption Criteria
n/a

## 7. Deliverables
### 7.1	Test Evaluation Summaries
The test run summary is available in each TeamCity build.  
A badge of the build status can be found [here](https://github.com/keycloud/keycloud/blob/master/README.md).
### 7.2	Reporting on Test Coverage
The test coverage is availabe in the log of each TeamCity build, because TeamCity does not currently support the export of the Golang test suite.
### 7.3	Perceived Quality Reports
A quality report is availabe in each TeamCity build.  
More information can be found [here](https://teamcity.zeekay.dev/project.html?projectId=Keycloud&tab=stats). To login, please use the guest user.
### 7.4	Incident Logs and Change Requests
Incident logs are available in TeamCity.
### 7.5	Smoke Test Suite and Supporting Test Scripts
n/a
### 7.6	Additional Work Products
#### 7.6.1	Detailed Test Results
The detailed test results are available in each TeamCity build.
#### 7.6.2	Additional Automated Functional Test Scripts
n/a
#### 7.6.3	Test Guidelines
n/a
#### 7.6.4	Traceability Matrices
n/a

## 8. Testing Workflow
Developers should execute tests locally before pushing source code. When pushing to master, tests are executed automatically.
## 9. Environmental Needs
This section presents the non-human resources required for the Test Plan.
### 9.1	Base System Hardware
The following table sets forth the system resources for the test effort presented in this Test Plan.

| Resource | Quantity | Name and Type |
|---|---|---|
| TeamCity instance | 1 | TeamCity running the tests |
| URL |  	| https://teamcity.zeekay.dev/ |

### 9.2	Base Software Elements in the Test Environment
The following base software elements are required in the test environment for this Test Plan.

| Software Element Name | Version | Type and Other Notes |
|---|---|---|
| Linux |  v4.18.0 | Operating System |
| Golang | | Programming language |
| Angular | >v.9.0.0 | Framework |

### 9.3	Productivity and Support Tools
The following tools will be employed to support the test process for this Test Plan.

| Tool Category or Type | Tool Brand Name                              |
|-----------------------|----------------------------------------------|
| Code Hoster           | [github.com](https://github.com/keycloud) |
| CI Service            | [TeamCity](https://teamcity.zeekay.dev/) |

### 9.4	Test Environment Configurations
n/a

## 10. Responsibilities, Staffing, and Training Needs
### 10.1 People and Roles
This table shows the staffing assumptions for the test effort.

Human Resources


| Role | Minimum Resources Recommended (number of full-time roles allocated) |	Specific Responsibilities or Comments |
|---|---|---|
| Test Manager | 1 | Provides management oversight. <br> Responsibilities include: <br> planning and logistics <br> agree mission <br> identify motivators<br> acquire appropriate resources<br> present management reporting<br> advocate the interests of test<br>evaluate effectiveness of test effort |
| Test Designer | 1 | Defines the technical approach to the implementation of the test effort. <br> Responsibilities include:<br> define test approach<br> define test automation architecture<br> verify test techniques<br> define testability elements<br> structure test implementation|
| Tester | 1 |	Implements and executes the tests.<br> Responsibilities include:<br> implement tests and test suites<br> execute test suites<br> log results<br> analyze and recover from test failures<br> document incidents|
| Implementer | 3 | Implements and unit tests the test classes and test packages.<br> Responsibilities include:<br> creates the test components required to support testability requirements as defined by the designer |

### 10.2 Staffing and Training Needs
**n/a**
## 11. Iteration Milestones

| Milestone | Planned Start Date | Actual Start Date | Planned End Date | Actual End Date |
|---|---|---|---|---|
| Have Unit Tests | 01.04.2020 | since start of development | 04.06.2020 | **tbd**   |
| Tests integrated in CI | 01.05.2020 | 08.05.2020 | 04.06.2020 | **tbd** |


## 12. Risks, Dependencies, Assumptions, and Constraints
| Risk | Mitigation Strategy	| Contingency (Risk is realized) |
|---|---|---|
| Unexpected failures in production | Cover all important functions in tests | Rollback deployment to last stable version |
## 13. Management Process and Procedures
### 13.1 Deployment and Metrics
1. Run TeamCity Build, includes the runners to find the metrics and the build of the server, frontend application and Android Autofiller.
2. If all previous steps succeed, the docker image is build and deployed to docker hub. This image is then deployed as the new live version of the application.