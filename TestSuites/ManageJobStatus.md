# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.
- Navigate to <https://cte-dev.iclick.nz/>
- Login as the user in [User Data](..\TestData\UserData.md) file.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/job-status>

## After Each Test case

- Close the web browser.

## Test Cases

## TC 030 - Verify Navigate to Job Status Page

### Priority TC 030 : High

- Navigate to Job Status
- Verify Job Status page opens
- Verify page URL contains "/job-status"
- Verify page title displays "Settings-Job Status"

## TC 031 - Verify View Existing Job Statuses

### Priority TC 031 : High

- Verify job status list displays
- Verify table shows status names
- Verify table shows active status
- Verify table shows action buttons
- Verify pagination functionality works
- Verify showing results information displays

## TC 032 - Edit Job Status Name and Colors

### Priority TC 032 : High

- Select any existing job status
- Click edit action button
- Change status name to "Updated Progress"
- Set background color to "CFFFE2"
- Set font color to "1B3C53"
- Click Save button
- Verify success message appears
- Verify updated status displays in list
- Verify new name shows as "Updated Progress"
- Verify colors are applied correctly

## TC 033 - Add new job status

- Click on the "+ Status" button
- Set status name to "Waiting"
- Set background color to "FFFBDE"
- Set font color to "0D5EA6"
- Click Save button
- Verify success message appears
- Verify updated status displays in list
- Verify name shows as "Waiting"
- Verify colors are applied correctly

## TC 034 - Delete Job Status

### Priority TC 034 : High

- Select any existing job status from the list
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

## TC 035 - Cancel Delete Job Status

### Priority TC 035 : High

- Select any existing job status from the list
- Click the action menu (⋮) for the selected status  
- Click "Delete" from the dropdown menu
- Verify confirmation dialog appears
- Click "Cancel" button
- Verify dialog closes
- Verify job status remains in the list (not deleted)
- Verify no success or error message appears
- Verify total count of statuses remains unchanged
