# Feature: Search and View a Contract Profile Assignment

# Key
RAIL-104

# Description
  As a Contract Specialist,
  I want to search a Contract Profile Assignment
  so that I can view all the main information for that record.

# Acceptance Criteria

Background:
  Given the user navigates to the Contract Profile URL
  Then the header "Contract Profile" is displayed
  And the search criteria fields are displayed:
    | Assignment | Customer |
  And the corresponding labels are displayed:
    | Assignment | Customer |
  And the expected columns are displayed:
    | Assignment | Customer | Car Count |
  And 0 row(s) are displayed on the Assignment results table
  And the message "no records" is displayed

@SearchViewDetailsPage
Scenario: Search a Contract Profile Assignment and view the Details page
  When the user enters the value <searchvalue> into the search criteria field <assignmentField>
  And the user clicks the Search button
  Then 1 row is displayed on the Assignment results table

  When the user clicks the assignment <assignment> in the Assignment column
  Then the Contract Profile Details tab is displayed
  And the expected value <assignmentValue> for the field <assignmentField> is displayed
  And the expected value <customerValue> for the field <customerField> is displayed
  And the expected value <carcountValue> for the field <carcountFieldField> is displayed

## Assumption
The navigation the the Contract Profile page is already available and tested.
Authentication and permissions are not yet implemented.