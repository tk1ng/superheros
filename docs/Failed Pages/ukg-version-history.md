---
title: UKG - Version History
deprecated: false
hidden: true
metadata:
  robots: index
---


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