# Feature: Search Contract Profile Record(s)

## Key
RAIL-102

## Description
  As a Contract Specialist
  I want to enter values in the search fields and perform a search
  So that I can view the Contract Profile records that I need to work on

## Acceptance Criteria

Background:
  Given the user navigates to the Contract Profile URL
  And the header "Contract Profile" is displayed
  And the search criteria fields are displayed:
    | Assignment | Customer |
  And the corresponding labels are displayed:
    | Assignment | Customer |
  And the expected columns are displayed:
    | Assignment | Customer | Car Count |
  And 0 row(s) are displayed on the Assignment results table
  And the message "no records" is displayed

@NoResults
Scenario: Search using criteria and view the Assignment table with no rows
  When the user enters the value(s) <value> in the search field(s) <field>
  And the user clicks the Search button
  Then 0 row(s) are displayed on the Assignment results table
  And the message "no records" is displayed

@WithResults
Scenario: Search using criteria and view the Assignment table with rows
  When the user enters the value(s) <value> in the search field(s) <field>
  And the user clicks the Search button
  Then <rows> row(s) are displayed on the Assignment results table
  And the row(s) are displayed with expected row number <row>, values <values>, for the column headers <headers>

## Assumption
The navigation the the Contract Profile page is already available and tested.
Authentication and permissions are not yet implemented.
