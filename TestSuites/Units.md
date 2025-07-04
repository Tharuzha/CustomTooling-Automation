# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.
- Navigate to <https://cte-dev.iclick.nz/>
- Login as the user in [User Data](..\TestData\UserData.md) file.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/units>

## After Each Test case

- Close the web browser.

## Test Cases

## TC 046 - Verify Navigate to Units Page

### Priority TC 046 : High

- Navigate to Units
- Verify Units page opens
- Verify page URL contains "/units"
- Verify page title displays "Settings-Units"

## TC 047 - Verify View Existing Units

### Priority TC 047 : High

- Verify units list displays
- Verify table shows unit symbols
- Verify table shows unit descriptions
- Verify table shows action buttons
- Verify pagination functionality works
- Verify showing results information displays

## TC 048 - Add New Unit

### Priority TC 048 : High

- Click on the "+ Unit" button
- Set unit name to "Kilogram"
- Set description to "Unit of mass measurement"
- Click Save button
- Verify success message appears
- Verify new unit displays in list
- Verify unit name shows as "Kilogram"
- Verify description shows as "Unit of mass measurement"

## TC 049 - Edit Existing Unit

### Priority TC 049 : High

- Select any existing unit from the list
- Click edit action button
- Change unit name to "ml"
- Change description to "Updated unit for length measurement"
- Click Save button
- Verify success message appears
- Verify updated unit displays in list
- Verify new name shows as "ml"
- Verify new description shows as "Updated unit for length measurement"

## TC 050 - Verify Unit Name Field is Mandatory

### Priority TC 050 : High

- Click on the "+ Unit" button
- Leave unit name field empty
- Set description to "Test description"
- Click Save button
- Verify validation error appears: "The unit field is required."
- Verify dialog remains open
- Enter unit name "Test Unit"
- Click Save button
- Verify unit is successfully saved

## TC 051 - Verify Description Field is Mandatory

### Priority TC 051 : High

- Click on the "+ Unit" button
- Set unit name to "Test Unit"
- Leave description field empty
- Click Save button
- Verify validation error appears: "The description field is required."
- Verify dialog remains open
- Set description to "Test description"
- Click Save button
- Verify unit is successfully saved

## TC 052 - Delete Unit

### Priority TC 052 : High

- Select any existing unit from the list
- Click the action menu (⋮) for the selected unit
- Click "Delete" from the dropdown menu
- Verify confirmation dialog appears
- Verify dialog shows "Are you sure?" message
- Verify dialog shows "This action cannot be undone." warning
- Verify dialog has "Yes, delete it!" and "Cancel" buttons
- Click "Yes, delete it!" button
- Verify success message appears
- Verify deleted unit no longer appears in the list
- Verify total count of units is reduced by 1

## TC 053 - Cancel Delete Unit

### Priority TC 053 : High

- Select any existing unit from the list
- Click the action menu (⋮) for the selected unit
- Click "Delete" from the dropdown menu
- Verify confirmation dialog appears
- Click "Cancel" button
- Verify dialog closes
- Verify unit remains in the list (not deleted)
- Verify no success or error message appears
- Verify total count of units remains unchanged
