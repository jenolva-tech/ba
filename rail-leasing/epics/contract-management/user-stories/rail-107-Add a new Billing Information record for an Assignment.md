# Add a new Billing Information record for an Assignment

# Key
RAIL-107

# Description
As a Contract Specialist,
I want to enter the billing information for an Assignment
so that the system can store accurate Start, Stop, Rent, Maintenance, and Notes details for billing and contract management.

# Acceptance Criteria

Background:
  Given the user navigates to the Contract Profile URL
  And the user enters the value <searchValue> into the search criteria field <assignmentField>
  And the user clicks the Search button
  Then 1 row is displayed on the Assignment results table

  When the user clicks the assignment <assignment> in the Assignment column
  Then the Contract Profile Details tab is displayed
  And the expected value <assignmentValue> for the field <assignmentField> is displayed

  When the user clicks the Billing tab
  Then the header "Billing" is displayed
  And a table is displayed with columns:
    | Start | Stop | Rent | Maintenance | Notes |

@AddNewEmptyRow
Scenario: Add a new empty row in the Billing table
  When the user clicks the Add icon
  Then 1 row is inserted with empty columns

@AddNewRow
Scenario: Add a new row in the Billing table and save
  When the user clicks the Add icon
  Then 1 row is inserted with empty columns

  When the user updates the fields:
    | Start | Stop | Rent | Maintenance | Notes |
    with values <values>
  And the user clicks the Save icon
  Then the Billing record is saved and displayed with the updated values

## Assumption
The navigation to the Contract Profile page is already available and tested.
Authentication and permissions are not yet implemented.
The Contract Profile search page/main page, results table are available and tested.
The Contract Profile tab is completed, available and tested.