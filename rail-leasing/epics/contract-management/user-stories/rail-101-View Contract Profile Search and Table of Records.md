# View Contract Profile Search and Records Table
(Who, What, Why)

## Key
RAIL-101

## Description
As a Contract Specialist,
I want to view the search criteria page and the results table
so that I know where contract records will appear once I perform a search

## Acceptance Criteria

### Scenario 1: Navigate to Contract Profile Page and see search criteria and an empty results table
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

## Assumption
The navigation to the Contract Profile page is already available and tested.
Authentication and permissions are not yet implemented.