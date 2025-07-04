# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.
- Navigate to <https://cte-dev.iclick.nz/>
- Login as the user in [User Data](..\TestData\UserData.md) file.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/quote-status>

## After Each Test case

- Close the web browser.

## Test Cases

## TC 036 - Verify Navigate to Quote Status Page

### Priority TC 036 : High

- Navigate to Quote Status
- Verify Quote Status page opens
- Verify page URL contains "/quote-status"
- Verify page title displays "Settings-Quote Status"

## TC 037 - Verify View Existing Quote Statuses

### Priority TC 037 : High

- Verify quote status list displays
- Verify table shows quote status names
- Verify table shows active status
- Verify table shows action buttons
- Verify pagination functionality works
- Verify showing results information displays

## TC 038 - Edit Quote Status Name and Colors

### Priority TC 038 : High

- Select any existing quote status
- Click edit action button
- Change status name to "Updated Expired"
- Set background color to "CFFFE2"
- Set font color to "1B3C53"
- Click Save button
- Verify success message appears
- Verify updated status displays in list
- Verify new name shows as "Updated Expired"
- Verify colors are applied correctly

## TC 039 - Add new quote status

### Priority TC 039 : High

- Click on the "+ Status" button
- Set status name to "Waiting For Approval"
- Set background color to "FFFBDE"
- Set font color to "0D5EA6"
- Click Save button
- Verify success message appears
- Verify updated status displays in list
- Verify name shows as "Waiting"
- Verify colors are applied correctly

## TC 040 - Verify All Required Fields Validation

### Priority TC 040 : High

- Click on the "+ Status" button
- Leave all fields empty (Status name, Font Color, Background Color)
- Click Save button
- Verify validation errors appear for all required fields:
  - "The status field is required."
  - "The font color field is required."
  - "The background color field is required."
- Verify dialog remains open
- Verify status is not saved to the list

## TC 041 - Verify Status Name Field Only Validation

### Priority TC 041 : High

- Click on the "+ Status" button
- Leave status name field empty
- Set font color to "#0D5EA6"
- Set background color to "#FFFBDE"
- Click Save button
- Verify validation error appears: "The status field is required."
- Verify no errors for color fields
- Verify dialog remains open
- Enter status name "Test Status"
- Click Save button
- Verify status is successfully saved

## TC 042 - Verify Font Color Field Validation

### Priority TC 042 : High

- Click on the "+ Status" button
- Set status name to "Test Font Color"
- Leave font color field empty
- Set background color to "#FFFBDE"
- Click Save button
- Verify validation error appears: "The font color field is required."
- Verify dialog remains open
- Set font color to "#0D5EA6"
- Click Save button
- Verify status is successfully saved

## TC 043 - Verify Background Color Field Validation

### Priority TC 043 : High

- Click on the "+ Status" button
- Set status name to "Test Background Color"
- Set font color to "#0D5EA6"
- Leave background color field empty
- Click Save button
- Verify validation error appears: "The background color field is required."
- Verify dialog remains open
- Set background color to "#FFFBDE"
- Click Save button
- Verify status is successfully saved

## TC 044 - Delete Quote Status

### Priority TC 044 : High

- Select any existing quote status from the list
- Click the action menu (⋮) for the selected status
- Click "Delete" from the dropdown menu
- Verify confirmation dialog appears
- Verify dialog shows "Are you sure?" message
- Verify dialog shows "This action cannot be undone." warning
- Verify dialog has "Yes, delete it!" and "Cancel" buttons
- Click "Yes, delete it!" button
- Verify success message appears
- Verify deleted status no longer appears in the list
- Verify total count of statuses is reduced by 1

## TC 045 - Cancel Delete Quote Status

### Priority TC 045 : High

- Select any existing quote status from the list
- Click the action menu (⋮) for the selected status  
- Click "Delete" from the dropdown menu
- Verify confirmation dialog appears
- Click "Cancel" button
- Verify dialog closes
- Verify quote status remains in the list (not deleted)
- Verify no success or error message appears
- Verify total count of statuses remains unchanged
