# View the Billing Information of an Assignment

# Key
RAIL-106

# Description
As a Contract Specialist,
I want to view the Billing information for an Assignment
so that I can review the Start, Stop, Rent, Maintenance, and Notes details associated with that Assignment.

# Acceptance Criteria

## Scenario 1: View the Billing Tab with an empty table
Given the user navigates to the Contract Profile URL
When the user enters the value {value} into the search criteria field(s) {Assignment}
And the user clicks the button Save
Then 1 row(s) is displayed on the Assignment results table

When the user clicks the assignment {assignment} on the column Assignment
Then the Contract Profile Main tab is displayed
And the expected values {value} for the fields {Assignment} are displayed

When the user clicks the Billing tab
Then the header "Billing" is displayed
And a table is displayed with columns:
| Start | Stop | Rent | Maintenance | Notes |
And 0 row(s) are displayed on the Billing results table

## Scenario 2: View the Billing Tab with row(s)
GGiven the user navigates to the Contract Profile URL
When the user enters the value {value} into the search criteria field(s) {Assignment}
And the user clicks the button Save
Then 1 row(s) is displayed on the assignment results table

When the user clicks the assignment {assignment} on the column Assignment
Then the Contract Profile Main tab is displayed
And the expected values {value} for the fields {Assignment} are displayed

When the user clicks the Billing tab
Then the header "Billing" is displayed
And a table is displayed with columns:
| Start | Stop | Rent | Maintenance | Notes |
And {rows} row(s) are displayed on the Billing results table
And row(s) are displayed with expected row number {row}, values {values} for the column headers {headers}

## Assumption
The navigation to the Contract Profile page is already available and tested.
Authentication and permissions are not yet implemented.
The Contract Profile search page/main page, results table are available and tested.
The Contract Profile tab is completed, available and tested.
