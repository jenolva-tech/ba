# Search a Contract Profile Assignment

# Key
RAIL-104

# Description
As a Contract Specialist,
I want to search a Contract Profile Assignment
so that I can view all the main information for that record

# Acceptance Criteria

## Scenario 1: Search a Contract Profile Assignment and view Details Page
Given the user navigates to the Contract Profile URL
When the user enters the value {value} into the search criteria field(s) {Assignment}
And the user clicks the button Save
Then 1 row is displayed on the results table
When the user clicks the assignment {assignment} on the column Assignment
Then the Contract Profile Main tab is displayed
And the expected values {values} for the fields {fields} are displayed