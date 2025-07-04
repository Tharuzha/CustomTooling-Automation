# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.
- Navigate to <https://cte-dev.iclick.nz/>
- Login as the user in [User Data](..\TestData\UserData.md) file.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/routing>

## After Each Test case

- Close the web browser.

## Test Cases

## TC 067 - Verify Navigate to Routing Page

### Priority TC 067 : High

- Navigate to Routing
- Verify Routing page opens
- Verify page URL contains "/routing"
- Verify page title displays "Settings - Routing"

## TC 068 - Verify View Existing Routing

### Priority TC 068 : High

- Verify routing list displays
- Verify table shows routing names
- Verify table shows order numbers
- Verify table shows descriptions
- Verify table shows hourly rates
- Verify table shows divisions
- Verify table shows status (Active/Inactive)
- Verify table shows action buttons
- Verify pagination functionality works
- Verify showing results information displays

## TC 069 - Add New Routing

### Priority TC 069 : High

- Click on the "+ Routing" button
- Set order to "15"
- Set routing name to "Assembly Line"
- Set description to "Product assembly process"
- Set hourly rate to "25.00"
- Select division "Main" from dropdown
- Select status "Active" from dropdown
- Click Save button
- Verify success message appears
- Verify new routing displays in list
- Verify routing name shows as "Assembly Line"
- Verify order shows as "15"
- Verify status shows as "Active"

## TC 070 - Edit Existing Routing

### Priority TC 070 : High

- Select any existing routing from the list
- Click edit action button
- Change order to "20"
- Change routing name to "Updated Process"
- Change description to "Updated process description"
- Change hourly rate to "30.00"
- Change status to "Inactive"
- Click Save button
- Verify success message appears
- Verify updated routing displays in list
- Verify new name shows as "Updated Process"
- Verify new order shows as "20"
- Verify status shows as "Inactive"

## TC 071 - Verify Order Field is Mandatory

### Priority TC 071 : High

- Click on the "+ Routing" button
- Leave order field empty
- Set routing name to "Test Routing"
- Set description to "Test description"
- Set hourly rate to "15.00"
- Select division "Main"
- Select status "Active"
- Click Save button
- Verify validation error appears: "The order field is required."
- Verify dialog remains open
- Enter order "10"
- Click Save button
- Verify routing is successfully saved

## TC 072 - Verify Routing Name Field is Mandatory

### Priority TC 072 : High

- Click on the "+ Routing" button
- Set order to "12"
- Leave routing name field empty
- Set description to "Test description"
- Set hourly rate to "15.00"
- Select division "Main"
- Select status "Active"
- Click Save button
- Verify validation error appears: "The routing field is required."
- Verify dialog remains open
- Set routing name to "Test Routing"
- Click Save button
- Verify routing is successfully saved

## TC 073 - Delete Routing

### Priority TC 073 : High

- Select any existing routing from the list
- Click the action menu (⋮) for the selected routing
- Click "Delete" from the dropdown menu
- Verify confirmation dialog appears
- Verify dialog shows "Are you sure?" message
- Verify dialog shows "This action cannot be undone." warning
- Verify dialog has "Yes, delete it!" and "Cancel" buttons
- Click "Yes, delete it!" button
- Verify success message appears
- Verify deleted routing no longer appears in the list
- Verify total count of routing is reduced by 1

## TC 074 - Cancel Delete Routing

### Priority TC 074 : High

- Select any existing routing from the list
- Click the action menu (⋮) for the selected routing
- Click "Delete" from the dropdown menu
- Verify confirmation dialog appears
- Click "Cancel" button
- Verify dialog closes
- Verify routing remains in the list (not deleted)
- Verify no success or error message appears
- Verify total count of routing remains unchanged

## TC 075 - Verify Search Functionality

### Priority TC 075 : High

- Verify routing list displays with multiple routings
- Note the total number of routings showing
- Enter "Inventory" in the search box
- Verify search filters the results
- Verify only routings with "Inventory" in routing name, description, hourly rate, or division are shown
- Verify routings not matching "Inventory" are hidden
- Clear the search box
- Next Enter "12.30" in the search box (search by hourly rate)
- Verify only routings with "12.30" hourly rate are shown
- Clear the search box
- Next Enter "Main" in the search box (search by division)
- Verify only routings with "Main" division are shown
- Clear the search box
- Next Enter "Repair" in the search box (search by description)
- Verify only routings with "Repair" in description field are shown
- Clear the search box
- Verify all routings display again
- Verify results count returns to original total

## TC 076 - Verify Search with No Results

### Priority TC 076 : High

- Enter "NonExistentRouting" in the search box
- Verify no routings are displayed in the list
- Verify "No results found" or similar message appears
- Verify results count shows 0 routings
- Clear the search box
- Verify all routings display again
- Verify results count returns to original total

## TC 077 - Verify Filter Functionality

### Priority TC 077 : High

- Click on "Filters" button
- Verify filter options appear
- Apply filter for "Active" status only
- Verify only active routings are displayed
- Verify inactive routings are hidden
- Apply filter for "Inactive" status only
- Verify only inactive routings are displayed
- Verify active routings are hidden
- Clear all filters
- Verify all routings display again
