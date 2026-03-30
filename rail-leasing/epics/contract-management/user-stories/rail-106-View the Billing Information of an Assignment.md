# Feature: View the Billing Information for an Assignment

# Key
RAIL-106

# Description
  As a Contract Specialist,
  I want to view the Billing information for an Assignment
  so that I can review the Start, Stop, Rent, Maintenance, and Notes details associated with that Assignment.

# Acceptance Criteria

Feature: View Billing Information for an Assignment
  As a Contract Specialist
  I want to view the Billing information for an Assignment
  So that I can review the Start, Stop, Rent, Maintenance, and Notes details

Background:
  Given the user navigates to the Contract Profile URL
  And the user enters the value <value> into the search criteria field <assignmentField>
  And the user clicks the Search button
  Then 1 row is displayed on the Assignment results table
  When the user clicks the assignment <assignment> in the Assignment column
  Then the Contract Profile Details tab is displayed
  And the expected value <value> for the field <assignmentField> is displayed

@BillingNoRows
Scenario: View the Billing tab with no rows
  When the user clicks the Billing tab
  Then the header "Billing" is displayed
  And a table is displayed with columns:
    | Start | Stop | Rent | Maintenance | Notes |
  And 0 row(s) are displayed on the Billing results table

@BillingWithRows
Scenario: View the Billing tab with rows
  When the user clicks the Billing tab
  Then the header "Billing" is displayed
  And a table is displayed with columns:
    | Start | Stop | Rent | Maintenance | Notes |
  And <rows> row(s) are displayed on the Billing results table
  And the row(s) are displayed with expected row number <row>, values <values>, for the column headers <headers>

## Assumption
The navigation to the Contract Profile page is already available and tested.
Authentication and permissions are not yet implemented.
The Contract Profile search page/main page, results table are available and tested.
The Contract Profile tab is completed, available and tested.
