# Feature: View Contract Profile Search and Results
(Who, What, Why)

## Key
RAIL-101

## Description
  As a Contract Specialist,
  I want to view the search criteria page and the results table
  so that I know where contract records will appear once I perform a search

## Acceptance Criteria

Background:
  Given the user navigates to the Contract Profile URL
  Then the header "Contract Profile" is displayed
  And the search criteria fields are displayed:
    | Assignment | Customer |
  And the corresponding labels are displayed:
    | Assignment | Customer |
  And the expected Contract table columns are displayed:
    | Assignment | Customer | Car Count |
  And 0 row(s) are displayed on the Assignment results table
  And the message "no records" is displayed

@InitialView
Scenario: View search criteria and Assignment table with no rows
  Then the Assignment results table displays 0 row(s)
  And the message "no records" is displayed

## Assumption
The navigation to the Contract Profile page is already available and tested
Authentication and permissions are not yet implemented