# Test automation questions

### Testing Basics (ISTQB related)

#### What is the purpose of testing? What is not?
The purpose of testing is to provide complete information to the stakeholders about technical or other restrictions, risk factors, ambiguous requirements
Not:
Finding bugs in the code
annoying developers and managers

#### What is the difference between Defect, Error, Failure?

Error - a mistake in coding
Defect - error found by the tester
Bug - Defect accepted by developer team
Failure - a build that does not meet the requirement

#### What are the testing principles?

1 Testing shows the presence of defects
2 Exhaustive testing is not possible
3 Early testing
4 Defect clustering
5 Pesticide paradox
6 Testing is context-dependent
7 Absence of errors fallacy

#### What is unit testing? Who is responibile to write unit tests?

unit tests test a function or a block
the developer is responsible for unit tests that wrote the code

#### What are Test Levels, what is the difference between them?

Unit testing
Component testing
integration testing
system testing
acceptance testing

#### What is the difference between verification and validation?

Verification is a static practice of verifying documents, design, code and program. 
Validation is a dynamic mechanism of validating and testing the actual product.

#### What are Testing Types, what is the difference between them?

Accessibility testing
Acceptance testing
Black box testing
End to end testing
Integration testing
Performance testing
Regression testing
Security testing
Unit testing
White-box testing

#### What is the difference between white box, grey boy and black box testing?

black box testing: a tester doesn't have any information about the internal working of the software system

white box testing: White-box testing is a testing technique which checks the internal functioning of the system. In this method, testing is based on coverage of code statements, branches, paths or conditions.

grey box testing: high kevek test with the knowledge of the inner functions/systems. Typically it is done for security reasons  


#### What is the difference between UAT (User Acceptance Testing) and System testing?

System testing is done to check whether the software or product meets the specified requirements or not. 
 It is done by both testers and developers.
 positive and negative test cases

Acceptance testing is the type of testing which is used to check whether the software meets the customer requirements or not.
 Acceptance testing is used by testers, stakeholders as well as clients.
 positive test cases



#### Mention the differences between Regression Testing, Smoke Testing and Retesting?
Retesing: Retesting is a type of software testing which tests about a particular bug after it has been fixed
The test cases for re-testing can not be automated.
Is only a part of the testing process if a defect or bug is found in the code.

Regression testing is about searching for defects, whereas retesting is about fixing specific defects that you've already found.
ideal for automation
Should always be a part of the testing process and performed each time code is changed and a software update is about to be released.

Smoke testing: Smoke Testing is a type of software testing which checks the deployed build is stable or not.
#### What is risk-based testing, whats the point of it?
#### What is the difference between Static and Dynamic Testing?
#### Compare V-modell, Waterfall, Agile from testing perspective!
#### What would you test in case of a simple webshop purchasing function (put items to cart, buy them)? Plan and reason your tests.

### Reporting, Bugs

#### What steps would you follow when you find a defect?
#### Talk about common test reports, and about their details.
#### What does a bug report contains?

title
severity/priority
description
environment
steps to reproduce
expected result
actual result
attachments (screenshots, videos, text)

#### How would you prioritize a bug?
I would see how frequent the bug would be in a live environment and how severe the bug would be.

### Test Automation, Selenium

#### Which testcases should be be automated and which shouldn't?
#### Describe a good automated test!
#### What is Selenium, Selenium IDE, Selenium WebDriver?
#### How can be web elements indentified?
#### How can you wait for elements, what can go wrong? Collect possible errors and root causes.
#### Compare POM and Keyword Driven Testing!
#### Whats the difference between TDD and BDD?
#### What is API testing and why would you use that?
#### What is Data Driven Testing and why is it useful?
#### What are the challenges and best practices with dynamically loading web elements?
#### What are the challenges of Mobile Test Automation?

### Advanced Topics

#### What is the difference between CI and CD?
#### Describe a Continuous Delivery!
#### Compare 2 popular CI systems, one of them should be Jenkins!
#### What is Docker, why is it useful?
#### Compare 2 popular Test Automation IDE, one of them should be Katalon Studio!