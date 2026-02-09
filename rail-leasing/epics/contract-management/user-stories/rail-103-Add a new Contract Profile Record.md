# Add a new Contract Profile Record

## Key
RAIL-103

## Description
As a Contract Specialist
I want to add a new Contact Profile record
so that the contract information is saved in the system.

## Acceptance Criteria

### Scenario 1: New Contract Profile Page is displayed with empty fields
Given the user navigates to the Contract Profile URL
When user clicks the Add Icon
Then the "Enter a New Contract Profile Record" header is displayed
And the expected fields {fields} and labels {labels} are displayed
And the fields are empty


### Scenario 1: Add a new Contract Profile Record and Save
Given the navigates to the Contract Profile URL
When the user clicks the Add Icon
Then the header "Contract Profile" is displayed
When the user enters the value(s) {values} into the fields {field}
And the user clicks the button Save
And the main page with header "Contract Profile" is displayed
And a new row is displayed with expected values {values} for the column headers {headers} 
