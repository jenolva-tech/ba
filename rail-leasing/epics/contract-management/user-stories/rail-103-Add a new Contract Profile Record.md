# Feature: Add a New Contract Profile Record

# Key
RAIL-103

## Description
  As a Contract Specialist
  I want to open the new Contract Profile form and save a new record
  So that I can add Contract Profile information into the system

## Acceptance Criteria

Background:
    Given the user navigates to the Contract Profile URL

  @ViewNewForm
  Scenario: New Contract Profile page is displayed with empty fields
    When the user clicks the Add Icon
    Then the header "Enter a New Contract Profile Record" is displayed
    And the expected fields <fields> and labels <labels> are displayed
    And all fields are empty

  @AddNewRecord
  Scenario: Add a new Contract Profile record and save
    When the user clicks the Add Icon
    And the header "Enter a New Contract Profile Record" is displayed
    And the user enters the value(s) <values> into the fields <fields>
    And the user clicks the Save button
    Then the main page with header "Contract Profile" is displayed
    And a new row is displayed with expected values <values> for the column headers <headers>


## Assumption
The navigation the the Contract Profile page is already available and tested.
Authentication and permissions are not yet implemented.
The Contract Profile search page/main page, results table are available and tested.
