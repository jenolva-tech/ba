# Update an existing Contract Profile Record (Details Tab)

# Key
RAIL-105

# Description
As a Contract Specialist,
I want to update a Contract Profile record
so that all new information and corrections for the contract is saved in the system

# Acceptance Criteria

## Scenario 1: Update a Contract Profile Record
Given a user navigate to the Contract Profile URL
When the user enters the value(s) {Assignment} into field(s) {Assignment}
And the user clicks the button Search
Then the for the assignment is displayed with matching values {values} on column headers {headers}
And the user clicks the value {Assignment} on the column field {Assignment}
Then the record is displayed on the details page
When the user updates with value(s) {values} into field(s) {fields}
And the user clicks the button Save
Then the values {values} of the fields {fields} are saved in the database
Then a confirmation message "Information Saved" is displayed
