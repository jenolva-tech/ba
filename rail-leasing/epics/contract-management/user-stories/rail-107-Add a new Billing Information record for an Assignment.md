# Add a new Billing Information record for an Assignment

# Key
RAIL-107

# Description
As a Contract Specialist,
I want to enter the billing information for an Assignment
so that the system can store accurate Start, Stop, Rent, Maintenance, and Notes details for billing and contract management.

# Acceptance Criteria

## Scenario 1: Add a new empty row in the billing table

Given the user navigates to the Contract Profile URL
When the user enters the value {value} into the search criteria field(s) {Assignment}
And the user clicks the button Save
Then 1 row(s) are displayed on the assignment results table
When the user clicks the assignment {assignment} on the column Assignment
Then the Contract Profile Main tab is displayed
And the expected values {value} for the fields {Assignment} are displayed
When the user clicks the Billing tab
Then the header "Billing" is displayed
And a table is displayed with columns:
 | Start | Stop | Rent | Maintenance | Notes |
When the user clicks the Add icon
Then 1 row is inserted with empty fields

## Scenario 2: Add a new Billing record and save

Given the user navigates to the Contract Profile URL
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
When the user clicks the Add icon
Then 1 row is inserted with empty fields
When the user updates the fields:
 | Start | Stop | Rent | Maintenance | Notes |
with value(s) {Values}
And the user clicks the Save icon
Then the Billing record is saved and displayed with the updated values

## Assumption
The navigation to the Contract Profile page is already available and tested.
Authentication and permissions are not yet implemented.
The Contract Profile search page/main page, results table are available and tested.
The Contract Profile tab is completed, available and tested.