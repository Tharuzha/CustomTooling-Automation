# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.
- Navigate to <https://cte-dev.iclick.nz/>
- Login as the user in [User Data](..\TestData\UserData.md) file.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/stock-location>

## After Each Test case

- Close the web browser.

## Test Cases

## TC 056 - Verify Navigate to Stock Locations Page

### Priority TC 056 : High

- Navigate to Stock Locations
- Verify Stock Locations page opens
- Verify page URL contains "/stock-location"
- Verify page title displays "Settings - Stock Locations"

## TC 057 - Verify View Existing Stock Locations

### Priority TC 057 : High

- Verify stock locations list displays
- Verify table shows stock location names
- Verify table shows status (Active/Inactive)
- Verify table shows action buttons
- Verify pagination functionality works
- Verify showing results information displays

## TC 058 - Add New Stock Location

### Priority TC 058 : High

- Click on the "+ Stock Location" button
- Select status "Active" from dropdown
- Set stock location name to "Warehouse A"
- Click Save button
- Verify success message appears
- Verify new stock location displays in list
- Verify location name shows as "Warehouse A"
- Verify status shows as "Active"

## TC 059 - Edit Existing Stock Location

### Priority TC 059 : High

- Select any existing stock location from the list
- Click edit action button
- Change status to "Inactive"
- Change stock location name to "Updated Storage"
- Click Save button
- Verify success message appears
- Verify updated stock location displays in list
- Verify new name shows as "Updated Storage"
- Verify status shows as "Inactive"

## TC 060 - Verify Status Field is Mandatory

### Priority TC 060 : High

- Click on the "+ Stock Location" button
- Leave status field as "Select a Status"
- Set stock location name to "Test Location"
- Click Save button
- Verify validation error appears: "The status field is required."
- Verify dialog remains open
- Select status "Active"
- Click Save button
- Verify stock location is successfully saved

## TC 061 - Verify Stock Location Field is Mandatory

### Priority TC 061 : High

- Click on the "+ Stock Location" button
- Select status "Active"
- Leave stock location name field empty
- Click Save button
- Verify validation error appears: "The stock location field is required."
- Verify dialog remains open
- Set stock location name to "Test Location"
- Click Save button
- Verify stock location is successfully saved

## TC 062 - Delete Stock Location

### Priority TC 062 : High

- Select any existing stock location from the list
- Click the action menu (⋮) for the selected location
- Click "Delete" from the dropdown menu
- Verify confirmation dialog appears
- Verify dialog shows "Are you sure?" message
- Verify dialog shows "This action cannot be undone." warning
- Verify dialog has "Yes, delete it!" and "Cancel" buttons
- Click "Yes, delete it!" button
- Verify success message appears
- Verify deleted stock location no longer appears in the list
- Verify total count of locations is reduced by 1

## TC 063 - Cancel Delete Stock Location

### Priority TC 063 : High

- Select any existing stock location from the list
- Click the action menu (⋮) for the selected location
- Click "Delete" from the dropdown menu
- Verify confirmation dialog appears
- Click "Cancel" button
- Verify dialog closes
- Verify stock location remains in the list (not deleted)
- Verify no success or error message appears
- Verify total count of locations remains unchanged

## TC 064 - Verify Search Functionality

### Priority TC 064 : High

- Verify stock locations list displays with multiple locations
- Note the total number of locations showing
- Enter "Bulk" in the search box
- Verify search filters the results
- Verify only locations with "Bulk" in name are shown
- Verify locations not matching "Bulk" are hidden
- Verify results count updates to show filtered results
- Clear the search box
- Verify all locations display again
- Verify results count returns to original total

## TC 065 - Verify Search with No Results

### Priority TC 065 : High

- Enter "NonExistentLocation" in the search box
- Verify no locations are displayed in the list
- Verify "No results found" or similar message appears
- Verify results count shows 0 locations
- Clear the search box
- Verify all locations display again
- Verify results count returns to original total

## TC 066 - Verify Filter Functionality

### Priority TC 066 : High

- Click on "Filters" button
- Verify filter options appear
- Apply filter for "Active" status only
- Verify only active locations are displayed
- Verify inactive locations are hidden
- Apply filter for "Inactive" status only
- Verify only inactive locations are displayed
- Verify active locations are hidden
- Clear all filters
- Verify all locations display again
