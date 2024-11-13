---
title: UKG - Version History
deprecated: false
hidden: true
metadata:
  robots: index
---


## 2024.R1

The following operations were added to the API in 2024.R1:

| Domain | Resource | Operation | Method | URL endpoint |
| ------ | -------- | --------- | ------ | ------------- |
| Recruiting | Applications | Retrieve Applications | GET | /{tenantalias}/api/applications |
| Recruiting | Applications | Create Application | POST | /{tenantalias}/api/applications |
| Recruiting | Applications | Retrieve Application by ID | GET | /{tenantalias}/api/applications/{applicationId} |
| Recruiting | Applications | Upload Application Document | POST | /{tenantalias}/api/applications/{applicationId}/documents |
| Recruiting | Applications | Retrieve Comments by Application ID | GET | /{tenantalias}/api/applications/{applicationId}/comments |
| Recruiting | Applications | Create Comment by Application ID | POST | /{tenantalias}/api/applications/{applicationId}/comments |
| Recruiting | Applications | Initiate Hire by Application ID | POST | /{tenantalias}/api/applications/{applicationId}/hire |
| Recruiting | Applications | Look Up EasyApply Application by Candidate, Opportunity, and Integration ID | POST | /{tenantalias}/api/applications-easy-apply-lookup |
| Recruiting | Application Disposition Events | Retrieve Application Disposition Events by Application ID | GET | /{tenantalias}/api/applications/{applicationId}/disposition-events |
| Recruiting | Application Disposition Events | Disposition Application by ID | POST | /{tenantalias}/api/applications/{applicationId}/disposition-events |
| Recruiting | Application Disposition Events | Retrieve Application Disposition Events | GET | /{tenantalias}/api/applications-disposition-events |
| Recruiting | Candidates | Retrieve Candidates | GET | /{tenantalias}/api/candidates |
| Recruiting | Candidates | Create Candidate | POST | /{tenantalias}/api/candidates |
| Recruiting | Candidates | Retrieve Candidate by ID | GET | /{tenantalias}/api/candidates/{candidateId} |
| Recruiting | Candidates | Retrieve Name and Email by Candidate ID | GET | /{tenantalias}/api/candidates/{candidateId}/user-name-email |
| Recruiting | Candidates | Retrieve Candidate by Email | POST | /{tenantalias}/api/candidates-lookup |
| Recruiting | Candidates | Upload Document by Candidate ID | POST | /{tenantalias}/api/candidates/{candidateId}/documents |
| Recruiting | Candidates | Retrieve Comments by Candidate ID | GET | /{tenantalias}/api/candidates/{candidateId}/comments |
| Recruiting | Candidates | Add Comment by Candidate ID | POST | /{tenantalias}/api/candidates/{candidateId}/comments |
| Recruiting | Candidates | Retrieve Behaviors by Candidate ID | GET | /{tenantalias}/api/candidates/{candidateId}/behaviors |
| Recruiting | Candidates | Add Behavior by Candidate ID | POST | /{tenantalias}/api/candidates/{candidateId}/behaviors |
| Recruiting | Candidates | Retrieve Educations by Candidate ID | GET | /{tenantalias}/api/candidates/{candidateId}/educations |
| Recruiting | Candidates | Add Education by Candidate ID | POST | /{tenantalias}/api/candidates/{candidateId}/educations |
| Recruiting | Candidates | Retrieve Motivations by Candidate ID | GET | /{tenantalias}/api/candidates/{candidateId}/motivations |
| Recruiting | Candidates | Add Motivation by Candidate ID | POST | /{tenantalias}/api/candidates/{candidateId}/motivations |
| Recruiting | Candidates | Retrieve Licenses by Candidate ID | GET | /{tenantalias}/api/candidates/{candidateId}/licenses |
| Recruiting | Candidates | Add License by Candidate ID | POST | /{tenantalias}/api/candidates/{candidateId}/licenses |
| Recruiting | Candidates | Retrieve Skills by Candidate ID | GET | /{tenantalias}/api/candidates/{candidateId}/skills |
| Recruiting | Candidates | Add Skill by Candidate ID | POST | /{tenantalias}/api/candidates/{candidateId}/skills |
| Recruiting | Candidates | Retrieve References by Candidate ID | GET | /{tenantalias}/api/candidates/{candidateId}/references |
| Recruiting | Candidates | Add Reference by Candidate ID | POST | /{tenantalias}/api/candidates/{candidateId}/references |
| Recruiting | Candidates | Retrieve Candidate Reference by ID | GET | /{tenantalias}/api/candidates/{candidateId}/references/{referenceId} |
| Recruiting | Candidates | Update Candidate Reference by ID | PUT | /{tenantalias}/api/candidates/{candidateId}/references/{referenceId} |
| Recruiting | Candidates | Retrieve Work Experiences by Candidate ID | GET | /{tenantalias}/api/candidates/{candidateId}/work-experience |
| Recruiting | Candidates | Add Work Experience by Candidate ID | POST | /{tenantalias}/api/candidates/{candidateId}/work-experience |
| Recruiting | Prehire Assessments and WOTC Surveys | Retrieve Assessment by ID | GET | /{tenantalias}/api/candidates/{candidateid}/assessments/{assessmentid} |
| Recruiting | Prehire Assessments and WOTC Surveys | Update Assessment by ID | PUT | /{tenantalias}/api/candidates/{candidateid}/assessments/{assessmentid} |
| Recruiting | Prehire Assessments and WOTC Surveys | Create Assessment by ID | POST | /{tenantalias}/api/candidates/{candidateId}/assessments |
| Recruiting | Prehire Assessments and WOTC Surveys | Retrieve Assessments by Candidate ID | GET | /{tenantalias}/api/candidates/{candidateId}/assessments |
| Recruiting | Background Checks | Retrieve Background Check Order Request | GET | /{tenantalias}/api/background-check-order-requests |
| Recruiting | Background Checks | Create Background Check | POST | /{tenantalias}/api/candidates/{candidateId}/background-checks |
| Recruiting | Background Checks | Retrieve Multiple Background Checks | GET | /{tenantalias}/api/candidates/{candidateId}/background-checks |
| Recruiting | Background Checks | Retrieve Background Check By ID | GET | /{tenantalias}/api/candidates/{candidateId}/background-checks/{backgroundCheckId} |
| Recruiting | Background Checks | Update Background Check | PUT | /{tenantalias}/api/candidates/{candidateId}/background-checks/{backgroundCheckId} |
| Recruiting | Background Checks | Retrieve Background Check Results Request | GET | /{tenantalias}/api/background-check-results-requests |
| Recruiting | Opportunities | Retrieve Opportunities | GET | /{tenantalias}/api/opportunities |
| Recruiting | Opportunities | Create Opportunity | POST | /{tenantalias}/api/opportunities |
| Recruiting | Opportunities | Retrieve Opportunity by ID | GET | /{tenantalias}/api/opportunities/{opportunityId} |
| Recruiting | Opportunities | Retrieve Opportunity Country Questions | GET | /{tenantalias}/api/opportunities/{opportunityId}/country-questions |
| Recruiting | Opportunities | Retrieve Opportunity Assessment by ID | GET | /{tenantalias}/api/opportunities/{opportunityId}/assessments/{opportunityAssessmentId} |
| Recruiting | Opportunities | Update Opportunity Assessment by ID | PUT | /{tenantalias}/api/opportunities/{opportunityId}/assessments/{opportunityAssessmentId} |
| Recruiting | Opportunities | Delete Opportunity Assessment by ID | DELETE | /{tenantalias}/api/opportunities/{opportunityId}/assessments/{opportunityAssessmentId} |
| Recruiting | Opportunities | Retrieve All Opportunity Assessments | GET | /{tenantalias}/api/opportunities/{opportunityId}/assessments |
| Recruiting | Opportunities | Create Opportunity Assessment | POST | /{tenantalias}/api/opportunities/{opportunityId}/assessments |
| Recruiting | Opportunities | Publish Opportunity by ID | POST | /{tenantalias}/api/opportunities/{opportunityId}/publish |
| Recruiting | Opportunities | Close Opportunity by ID | POST | /{tenantalias}/api/opportunities/{opportunityId}/close |
| Recruiting | Opportunities | Refresh Opportunity by ID | POST | /{tenantalias}/api/opportunities/{opportunityId}/refresh |
| Recruiting | Opportunities | Create Opportunity Screening Question | POST | /{tenantalias}/api/opportunities/{opportunityId}/screening-questions |
| Recruiting | Opportunities | Retrieve Opportunity Screening Questions | GET | /{tenantalias}/api/opportunities/{opportunityId}/screening-questions |
| Recruiting | Opportunities | Update Opportunity Screening Question by ID | PUT | /{tenantalias}/api/opportunities/{opportunityId}/screening-questions/{screeningQuestionId} |
| Recruiting | Opportunities | Deactivate Opportunity Screening Questions | PATCH | /{tenantalias}/api/opportunities/{opportunityId}/screening-questions/{screeningQuestionId} |
| Recruiting | Offers | Retrieve Offers | GET | /{tenantalias}/api/offers |
| Recruiting | Offers | Create Offer | POST | /{tenantalias}/api/offers |
| Recruiting | Offers | Retrieve Offer Actions by Offer ID | GET | /{tenantalias}/api/offers/{offerId}/offer-actions |
| Recruiting | Offers | Submit Offer for Approval by ID | POST | /{tenantalias}/api/offers/{offerId}/submit-for-approval |
| Recruiting | Configuration and Settings | Retrieve All Applicant Sources | GET | /{tenantalias}/api/applicant-sources |
| Recruiting | Configuration and Settings | Create Applicant Source | POST | /{tenantalias}/api/applicant-sources |
| Recruiting | Configuration and Settings | Retrieve Applicant Source by ID | GET | /{tenantalias}/api/applicant-sources/{applicantSourceId} |
| Recruiting | Configuration and Settings | Retrieve All Behaviors | GET | /{tenantalias}/api/behaviors |
| Recruiting | Configuration and Settings | Create Behavior | POST | /{tenantalias}/api/behaviors |
| Recruiting | Configuration and Settings | Retrieve Behavior by ID | GET | /{tenantalias}/api/behaviors/{behaviorId} |
| Recruiting | Configuration and Settings | Archive or Unarchive Behavior by ID | PATCH | /{tenantalias}/api/behaviors/{behaviorId} |
| Recruiting | Configuration and Settings | Retrieve All Disposition Reasons | GET | /{tenantalias}/api/disposition-reasons |
| Recruiting | Configuration and Settings | Create Disposition Reason | POST | /{tenantalias}/api/disposition-reasons |
| Recruiting | Configuration and Settings | Retrieve Disposition Reason by ID | GET | /{tenantalias}/api/disposition-reasons/{dispositionReasonId} |
| Recruiting | Configuration and Settings | Retrieve All Fields of Study | GET | /{tenantalias}/api/fields-of-study |
| Recruiting | Configuration and Settings | Retrieve Field of Study by ID | GET | /{tenantalias}/api/fields-of-study/{fieldOfStudyID} |
| Recruiting | Configuration and Settings | Retrieve All Job Boards | GET | /{tenantalias}/api/job-boards |
| Recruiting | Configuration and Settings | Retrieve Job Board by ID | GET | /{tenantalias}/api/job-boards/{jobBoardID} |
| Recruiting | Configuration and Settings | Retrieve All Legal Entities | GET | /{tenantalias}/api/legal-entities |
| Recruiting | Configuration and Settings | Retrieve Legal Entity by ID | GET | /{tenantalias}/api/legal-entities/{legalEntityId} |
| Recruiting | Configuration and Settings | Retrieve All Motivations | GET | /{tenantalias}/api/motivations |
| Recruiting | Configuration and Settings | Create Motivation | POST | /{tenantalias}/api/motivations |
| Recruiting | Configuration and Settings | Retrieve Motivation by ID | GET | /{tenantalias}/api/motivations/{motivationId} |
| Recruiting | Configuration and Settings | Archive or Unarchive Motivation by ID | PATCH | /{tenantalias}/api/motivations/{motivationId} |
| Recruiting | Configuration and Settings | Retrieve Physical Locations | GET | /{tenantalias}/api/physical-locations |
| Recruiting | Configuration and Settings | Create Physical Location | POST | /{tenantalias}/api/physical-locations |
| Recruiting | Configuration and Settings | Retrieve Physical Location by ID | GET | /{tenantalias}/api/physical-locations/{physicalLocationId} |
| Recruiting | Configuration and Settings | Archive or Unarchive Physical Location by ID | PATCH | /{tenantalias}/api/physical-locations/{physicalLocationId} |
| Recruiting | Configuration and Settings | Retrieve All Prefixes | GET | /{tenantalias}/api/prefixes |
| Recruiting | Configuration and Settings | Retrieve Prefix by ID | GET | /{tenantalias}/api/prefixes/{prefixID} |
| Recruiting | Configuration and Settings | Retrieve All Proficiency Levels | GET | /{tenantalias}/api/proficiency-levels |
| Recruiting | Configuration and Settings | Retrieve Proficiency Level by ID | GET | /{tenantalias}/api/proficiency-levels/{proficiencyLevelId} |
| Recruiting | Configuration and Settings | Retrieve All Recruiting Processes | GET | /{tenantalias}/api/recruiting-processes |
| Recruiting | Configuration and Settings | Retrieve Recruiting Process By ID | GET | /{tenantalias}/api/recruiting-processes/{recruitingProcessID} |
| Recruiting | Configuration and Settings | Retrieve All Suffixes | GET | /{tenantalias}/api/suffixes |
| Recruiting | Configuration and Settings | Retrieve Suffix By ID | GET | /{tenantalias}/api/suffixes/{suffixID} |
| Recruiting | Configuration and Settings | Retrieve All Tax Locations | GET | /{tenantalias}/api/locations |
| Recruiting | Configuration and Settings | Retrieve Tax Location by ID | GET | /{tenantalias}/api/locations/{locationId} |
| Recruiting | Configuration and Settings | Retrieve Org Units | GET | /{tenantalias}/api/org-units |
| Recruiting | Configuration and Settings | Retrieve Org Unit by ID | GET | /{tenantalias}/api/org-units/{orgUnitId} |
| Recruiting | Third Party Job Sites | Retrieve Third Party Job Site Postings by Integration ID | GET | /{tenantalias}/api/third-party-job-board-integrations/{integrationId}/postings |
| Recruiting | Third Party Job Sites | Retrieve Application Disposition Events by Third Party Job Site Integration ID | GET | /{tenantalias}/api/third-party-job-board-integrations/{integrationId}/application-disposition-events |

## August 2022

The following operations were added to the API in August 2022:

Domain                                    | Resource                                           | Operation                                                            | Method | URL endpoint
----------------                          | ----------------                                   | ----------------                                                     | ------ | ----------------
Personnel                                 | Employee Security User Details                     | Retrieve Employee Security User Details                              | GET    | /personnel/v1/employee-security-user-details
Personnel                                 | Employee Extended Elements                         | Retrieve Employee Extended Elements                                  | GET    | /personnel/v1/employee-extended-elements
Payroll                                   | Earnings History Base Elements                     | Retrieve Earnings History Base Elements                              | GET    | /payroll/v1/earnings-history-base-elements

## July 2022

The following operations were added to the API in July 2022:

Domain                                    | Resource                                           | Operation                                                            | Method | URL endpoint
----------------                          | ----------------                                   | ----------------                                                     | ------ | ----------------
Configuration                             | Benefits Reductions                                | Retrieve Benefit Reductions                                          | GET    | /configuration/v1/benefit-reduction
Configuration                             | Insurance Rate           		                   | Retrieve Insurance Rate                                              | GET    | /configuration/v1/insurance-rate
Configuration                             | Option Rate                                        | Retrieve Option Rate                                                 | GET    | /configuration/v1/option-rate
Configuration                             | Positions                                          | Retrieve Positions                                                   | GET    | /configuration/v1/positions
Configuration                             | Roles                                              | Retrieve Roles                                                       | GET    | /configuration/v1/roles
Configuration                             | Shift Codes                                        | Retrieve Shift Codes                                                 | GET    | /configuration/v1/shift-codes
Payroll                                   | Earnings History Base Elements                     | Retrieve Earnings History Base Elements                              | GET    | /payroll/v1/earnings-history-base-elements
Payroll                                   | Pay Group Pay Periods                              | Retrieve Pay Groups And Pay Periods                                  | GET    | /payroll/v1/paygroup-payperiods
Personnel                                 | Audit Details                                      | Retrieve Audit Detail                                                | GET    | /personnel/v1/audit-details
Personnel                                 | Dependent Deductions                               | Retrieve Dependent Deduction                                         | GET    | /personnel/v1/dep-deductions
Personnel                                 | Employee Cobra Details                             | Retrieve Employee Cobra Detail                                       | GET    | /personnel/v1/employee-cobra-details
Personnel                                 | Employee Deduction Benefit Option Change Date      | Retrieve Employee Deduction Benefit Option Change Date               | GET    | /personnel/v1/emp-deductions-benefit-option-change-date
Personnel                                 | Integration Audit Configuration                    | Retrieve Integration Audit Configuration                             | GET    | /personnel/v1/integration-audit-configuration
Personnel                                 | Business Structure Status                          | Retrieve Business Structure Status                                   | GET    | /personnel/v1/integration/kronos/business-structure-status
Personnel                                 | Employee Status                                    | Retrieve Employee Status                                             | GET    | /personnel/v1/integration/kronos/employee-status
Personnel                                 | Employee Profiles                                  | Retrieve Employee                                                    | GET    | /personnel/v1/integration/kronos/employee-profiles
Payroll                                   | Employee Pay Statement > CompanyPayStatement       | Retrieve Employee(s) Pay Statement Summaries                         | POST   | /payroll/v1/companies/pay-statements-summary
Payroll                                   | Employee Pay Statement > CompanyPayStatement       | Retrieve Employee(s) Pay Statements                                  | POST   | /payroll/v1/companies/pay-statements
Payroll                                   | Employee Pay Statement > EmployeePayStatement      | Retrieve Employee Pay Statements By Employee ID                      | POST   | /payroll/v1/employees/pay-statements
Payroll                                   | Employee Pay Statement > EmployeePayStatement      | Retrieve Last Pay Statement By Employee ID                           | POST   | /payroll/v1/employees/pay-statement/last
Payroll                                   | Employee Pay Statement > EmployeePayStatement      | Retrieve Employee Pay Statement by Pay ID                            | GET    | /payroll/v1/pay-statement/{PayIdentifier}
Configuration                             | Earnings Code > Earnings                           | Retrieve All Earnings Configurations                                 | GET    | /configuration/v1/earnings
Configuration                             | Earnings Code > Earnings                           | Retrieve Earnings Configurations By Parameter                        | GET    | /configuration/v1/earnings/{CalculationRule}/{TaxCategory}/{UseDeductionOffset}/{CountryCode}/{IncludeInShiftDifferential}/{IncludeInManualCheck}
Configuration                             | Earnings Code > Earnings                           | Retrieve Specific Earning Configuration                              | GET    | /configuration/v1/earnings/{EarningCode}

## June 2022

The following operations were added to the API in June 2022:

Domain                                    | Resource                                           | Operation                                                             | Method | URL endpoint
----------------                          | ----------------                                   | ----------------                                                      | ------ | ----------------
Payroll                                   | Payroll Deductions History                         | Retrieve Payroll Deduction History                                    | GET    | /payroll/v1/payroll-deductions-history)
Payroll                                   | Pay Register              		                   | Retrieve Pay Register                                                 | GET    | /payroll/v1/pay-register
Personnel                                 | Employee Deduction History Effective Change Date   | Retrieve Employee Deduction History Effective Change Date             | GET    | /personnel/v1/deduction-history-effective-change-dates
Personnel                                 | Open Enrollment Dependent Deductions               | Retrieve Open Enrollment Dependent Deduction                          | GET    | /personnel/v1/open-enrollment-dep-deductions
Personnel                                 | Position Report                                    | Retrieve Position Report                                              | GET    | /personnel/v1/position-report
Personnel                                 | User Preferences                                   | Retrieve User Preferences                                             | GET    | /personnel/v1/user-preferences
Personnel                                 | User Profile                                       | Retrieve User Profile                                                 | GET    | /personnel/v1/user-profile-details

The following operations were enhanced in the API in June 2022:

Domain                                    | Resource                                           | Operation                                                             | Method | URL endpoint
----------------                          | ----------------                                   | ----------------                                                      | ------ | ----------------
Configuration                             | Code Tables                                        | Retrieve Code Table                                                   | GET    | /configuration/v1/code-tables
Configuration                             | Code Tables                                        | Update Code Table                                                     | POST   | /configuration/v1/code-tables

## May 2022

The following operations were added to the API in May 2022:

Domain                                    | Resource                                           | Operation                                                             | Method | URL endpoint
----------------                          | ----------------                                   | ----------------                                                      | ------ | ----------------
Configuration                             | Tax Group Details                                  | Retrieve Tax Group                                                   | GET    | /configuration/v1/tax-groups
Personnel                                 | User Details              		                   | Retrieve User Details                                                | GET    | /personnel/v1/user-details
Configuration                             | Organization Reporting Category                    | Retrieve Organizational Reporting Category From Org Level Codes      | GET    | /configuration/v1/organization-reporting-category
Personnel                                 | Employee Supervisor Details                        | Retrieve Employee Supervisor Details                                 | GET    | /personnel/v1/employee-supervisor-details
Personnel                                 | Employee Multiple Positions                        | Retrieve Multiple Position Employees                                 | GET    | /personnel/v1/empl-multiple-positions
Personnel                                 | Open Enrollment Employee Deductions                | Retrieve Open Enrollment Deductions                                  | GET    | /personnel/v1/open-enrollment-emp-deductions
Personnel                                 | Employee Multiple Phone Numbers                    | Retrieve Multiple Phone Number Employees                             | GET    | /personnel/v1/employee-multi-phone-numbers
Personnel                                 | Employee Multiple Jobs                             | Retrieve Multiple Job Employees                                      | GET    | /personnel/v1/empl-multiple-jobs
Personnel                                 | Employee Deductions                                | Retrieve Employee Deductions From Benefits                           | GET    | /personnel/v1/empl-deductions
Configuration                             | Job Groups                                         | Retrieve Job Groups Using Job Group Codes                            | GET    | /configuration/v1/jobgroup
Personnel                                 | Employee Demographic Details                       | Retrieve Employee Demographic Details                                | GET    | /personnel/v1/employee-demographics-details
Configuration                             | Deduction Code                                     | Retrieve Deduction Configuration For Benefit Setup                   | GET    | /configuration/v1/deductions

## April 2022

The following operations were added to the API in April 2022:

Domain                                    | Resource                                           | Operation                                                            | Method | URL endpoint
----------------                          | ----------------                                   | ----------------                                                     | ------ | ----------------
Personnel                                 | User-Defined Fields                                | Retrieve User Designed Fields                                        | GET    | /personnel/v1/user-defined-fields
Personnel                                 | User-Defined Fields                                | Retrieve Single Company User Defined Fields                          | GET    | /personnel/v1/{companyId}/user-defined-fields
Personnel                                 | User-Defined Fields                                | Retrieve Single Employee In Single Company User Defined Fields       | GET    | /personnel/v1/{companyId}/employees/{employeeId}/user-defined-fields

## March 2022

The following operation was added to the API in March 2022:

Domain                                    | Resource                                           | Operation                                                             | Method | URL endpoint
----------------                          | ----------------                                   | ----------------                                                      | ------ | ----------------
Personnel                                 | Employee Employement Details                          | Retrieve Employee Employment Details                               | GET    | /personnel/v1/employee-employment-details

## July 2020

The following operations were added to the API in July 2020:

Domain                                    | Resource                                           | Operation                                                             | Method | URL endpoint
----------------                          | ----------------                                   | ----------------                                                      | ------ | ----------------
Personnel                                 | Platform Configuration Custom Fields Data         | Retrieve Platform Configuration Custom Fields and Values               | GET    | /personnel/v1/platform-configuration-fields/class-name/{className}
Personnel                                 | Platform Configuration Custom Fields Data         | Retrieve Platform Configuration Custom Fields and Values               | GET    | /personnel/v2/platform-configuration-fields/class-name/{className}

## December 2019

The following operations were added to the API in December 2019:

Domain                                    | Resource                                           | Operation                                                             | Method | URL endpoint
----------------                          | ----------------                                   | ----------------                                                      | ------ | ----------------
Personnel                                 | General Ledger Run Details                        | Retrieve General Ledger Run Details Filterable by runId and blockId    | GET    | /personnel/v2/general-ledger
Personnel                                 | General Ledger Run Details                        | Retrieve Specific Ledger Run Details                                   | GET    | /personnel/v2/general-ledger/{runId}

The following operations were enhanced in the API in December 2019:

Domain                                    | Resource                                           | Operation                                                                                   | Method | URL endpoint
----------------                          | ----------------                                   | ----------------                                                                            | ------ | ----------------
Personnel                                 | Employee Job History                              | Retrieve Employee Job History Detail Records                                                 | GET    | /personnel/v1/employee-job-history-details
Personnel                                 | Employee Job History                              | Retrieve Specific Job History Detail Record                                                  | GET    | /personnel/v1/employee-job-history-details/{systemId}
Payroll                                   | Employee Direct Deposit Details                   | Retrieve List Of Direct Deposit Information All US And Canada Employees                      | GET    | /payroll/v1/direct-deposit
Payroll                                   | Employee Direct Deposit Details                   | Retrieve List Of Direct Deposit Information For US And Canada Employees By Company           | GET    | /payroll/v1/{companyId}/direct-deposit
Personnel                                 | Employee Contact Details                          | Retrieve All Details For Persons Assigned To An Employee As Contacts                         | GET    | /personnel/v1/contacts
Personnel                                 | Employee Contact Details                          | Retrieve All Details For A Single Person Assigned To An Employee As A Contact                | GET    | /personnel/v1/contacts/{contactId}
Personnel                                 | Global Employee Direct Deposit                    | Retrieve Direct Deposit Information For All US And Canada Employees                          | GET    | /personnel/v1/employee-global-banks
Personnel                                 | Global Employee Direct Deposit                    | Retrieve Direct Deposit Information For All US And Canada Employees By Company               | GET    | /personnel/v1/employee-global-banks
Personnel                                 | Global Employee Localization                      | Retrieve Employee Specific Localization Information From Platform Configuration              | GET    | /personnel/v1/employee-global-localization-elements
Personnel                                 | Global Employee Payments And Deductions           | Retrieve Payment And Deduction Information Assigned To Global Pay Group and Pay Schedules    | GET    | /personnel/v1/employee-pay-deduction-elements
Personnel                                 | Employee Contracts                                | Retrieve Contract Data Assigned To Employees                                                 | GET    | /personnel/v1/employee-contract-details
Personnel                                 | Compensation Details                              | Retrieve Compensation And Pay Informatiom                                                    | GET    | /personnel/v1/compensation-details
Personnel                                 | Compensation Details                              | Retrieve Compensation And Pay Informatiom By Company                                         | GET    | /personnel/v1/companies/{companyId}/compensation-details
Personnel                                 | Compensation Details                              | Retrieve Compensation And Pay Informatiom By Company And Employee                            | GET    | /personnel/v1/companies/{companyId}/employees/{employeeId}/compensation-details
Personnel                                 | Compensation Details                              | Retrieve Compensation And Pay Informatiom By Employee                                        | GET    | /personnel/v1/compensation-details/{employeeId}
Personnel                                 | Employment Details                                | Retrieve Employment Data                                                                     | GET    | /personnel/v1/employment-details
Personnel                                 | Employment Details                                | Retrieve Employment Data By Company                                                          | GET    | /personnel/v1/companies/{companyId}/employment-details
Personnel                                 | Employment Details                                | Retrieve Employment Data By Company And Employee                                             | GET    | /personnel/v1/companies/{companyId)/employees/{employeeId}/employment-details
Personnel                                 | Person Details                                    | Retrieve Details On A Person Shared Across Companies                                         | GET    | /personnel/v1/person-details
Personnel                                 | Person Details                                    | Retrieve Person Details By Company                                                           | GET    | /personnel/v1/companies/{companyId}/person-details
Personnel                                 | Person Details                                    | Retrieve Person Details By Company And Employee                                              | GET    | /personnel/v1/companies/{companyId}/employees/{employeeId}/person-details
Personnel                                 | Person Details                                    | Retrieve Person Details By Employee                                                          | GET    | /personnel/v1/person-details/{employeeId}

## March 2019

The following operations were added to the API in March 2019:

Domain                                    | Resource                                           | Operation                               | Method | URL endpoint
----------------                          | ----------------                                   | ----------------                        | ------ | ----------------
Personnel                                 | Employee File Management                           | Retrieve                                | GET    | /personnel/v1/person-details
Personnel                                 | Employee Case Management                           | Retrieve                                | GET    | /personnel/v1/person-details