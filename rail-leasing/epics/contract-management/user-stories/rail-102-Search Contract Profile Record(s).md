# Search Contract Profile Record(s)

## Description
As a Contract Specialist
I want to enter values on the search fields and search
So that I can view the Contract Profile records that I need to work on.

## Acceptance Criteria

### Scenario 2: Search by Search Criteria and view the Assignment table with rows
Given the user navigates to Contract Profile url
Then the header "Contract Profile" is displayed
And the search criteria fields are displayed:
| Assignment | Customer |
And the corresponding labels are displayed:
| Assignment | Customer |
And the expected columns are displayed:
| Assignment | Customer | Car Count |
And 0 row(s) are displayed on the Assignment results table
And the message "no records" is displayed

When the user enters the value(s) {value} in the search field(s) {field}
And the user clicks the Search button
Then {rows} row(s) are displayed on the Assignment results table
And the expected data {data} is displayed for each matching row

### Scenario 1: Search by Search Criteria and view the Assignment table with no rows
Given the user navigates to Contract Profile url
Then the header "Contract Profile" is displayed
And the search criteria fields are displayed:
| Assignment | Customer |
And the corresponding labels are displayed:
| Assignment | Customer |
And the expected columns are displayed:
| Assignment | Customer | Car Count |
And 0 row(s) are displayed on the Assignment results table
And the message "no records" is displayed

When the user enters the value(s) {value} in the search field(s) {field}
And the user clicks the Search button
Then 0 row(s) are displayed on the Assignment results table
And the message "no records" is displayed


## Assumption
The navigation the the Contract Profile page is already available and tested.
Authentication and permissions are not yet implemented.
