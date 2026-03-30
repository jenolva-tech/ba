# Feature: Update an existing Contract Profile Record (Details Tab)

# Key
RAIL-105

# Description
As a Contract Specialist,
I want to update a Contract Profile record
so that all new information and corrections for the contract is saved in the system.

# Acceptance Criteria

Background:
  Given the user navigates to the Contract Profile URL
  And the user enters the value <searchValue> into the search criteria field <assignmentField>
  And the user clicks the Search button
  Then 1 row is displayed on the Assignment results table
  When the user clicks the assignment <assignment> in the Assignment column
  Then the Contract Profile Details tab is displayed
  And the expected value <assignmentValue> for the field <assignmentField> is displayed

@UpdateContractProfileRecord
Scenario: Update a Contract Profile record
  When the user updates the field <field> with value <value>
  And the user clicks the Save button
  Then the value <value> for the field <field> is saved in the database
  And a confirmation message "Information Saved" is displayed

## Assumption
The navigation the the Contract Profile page is already available and tested.
Authentication and permissions are not yet implemented.
The Contract Profile search page/main page, results table are available and tested.
The Contract Profile tab is with fields is available.
