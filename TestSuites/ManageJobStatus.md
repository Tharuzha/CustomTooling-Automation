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
