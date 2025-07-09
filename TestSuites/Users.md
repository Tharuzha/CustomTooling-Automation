# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.
- Navigate to <https://cte-dev.iclick.nz/>
- Login as the user in [User Data](..\TestData\UserData.md) file.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/users>

## After Each Test case

- Close the web browser.

## Test Cases

## TC 100 - Verify Navigate to Users Page

### Priority TC 100 : High

- Click on "Users & User Roles" dropdown button to expand the menu
- Navigate to Users
- Verify Users page opens
- Verify page URL contains "/users"
- Verify page title displays "Users"

## TC 101 - Verify Existing Users Data

### Priority TC 101 : High

- Navigate to Users
- Verify Users table is displayed with columns: User, Role, Status, Actions
- Verify at least one user is displayed in the table
- Verify each user entry contains:
  - User name and email address
  - Role information (admin, staff, etc.)
  - Status information (Active/Inactive)
  - Actions menu (⋮) available
- Verify result count is displayed and shows actual number of users
- Verify all user data is properly formatted and readable

## TC 102 - Adding New User as Staff Role

### Priority TC 102 : High

- Click "+User" button to open Add User form
- Should fill in required fields:
  - First Name: Enter valid first name
  - Last Name: Enter valid last name
  - Email: Enter valid email address
  - Role: Select "staff" from dropdown
  - Charge Rate: Enter appropriate hourly rate
  - Status: Select "Active" from dropdown
- Should fill in optional fields:
  - Position: Enter job position/title
  - Location: Enter work location
  - Show In Time Recorder: Check if applicable
- Click "Save" button to create user
- Verify success message "User created successfully!" appears
- Verify page redirects back to Users list
- Verify new user appears in the Users table with:
  - Correct name and email display
  - Role shows as "staff"
  - Status shows as "Active"
  - Actions menu (⋮) is available
- Verify user count increases by 1

## TC 103 - Adding New User as admin Role

### Priority TC 103 : High

- Click "+User" button to open Add User form
- Fill in required fields:
  - First Name: Enter valid first name
  - Last Name: Enter valid last name
  - Email: Enter valid email address
  - Role: Select "admin" from dropdown
  - Status: Select "Active" from dropdown
- Fill in optional fields:
  - Position: Enter job position/title
  - Location: Enter work location
- Click "Save" button to create user
- Verify success message "User created successfully!" appears
- Verify page redirects back to Users list
- Verify new user appears in the Users table with:
  - Correct name and email display
  - Role shows as "admin"
  - Status shows as "Active"
  - Actions menu (⋮) is available
- Verify user count increases by 1
- Verify all user data is properly formatted and readable

## TC 104 - Verify Mandatory Field Validation

### Priority TC 104 : High

- Click "+User" button to open Add User form
- Leave all mandatory fields empty:
  - First Name: Leave empty
  - Last Name: Leave empty
  - Email: Leave empty
  - Role: Leave as default "-"
  - Status: Leave as default "-"
- Click "Save" button to attempt user creation
- Verify form validation prevents saving
- Verify appropriate error messages are displayed for mandatory fields
- Verify user is not created and remains on Add User page
- Verify no success message appears
- Verify user count does not increase

## TC 105 - Adding New Admin User with Inactive Status

### Priority TC 105 : High

- Click "+User" button to open Add User form
- Fill in required fields:
  - First Name: Enter valid first name
  - Last Name: Enter valid last name
  - Email: Enter valid email address
  - Role: Select "admin" from dropdown
  - Status: Select "Inactive" from dropdown
- Fill in optional fields:
  - Position: Enter job position/title
  - Location: Enter work location
- Click "Save" button to create user
- Verify success message "User created successfully!" appears
- Verify page redirects back to Users list
- Verify new user appears in the Users table with:
  - Correct name and email display
  - Role shows as "admin"
  - Status shows as "Inactive"
  - Actions menu (⋮) is available
- Verify user count increases by 1

## TC 106 - Verify Search Functionality

### Priority TC 106 : High

- Locate search field on the page
- Test name search:
  - Should Enter partial first name of an existing user in search field
  - Verify table filters to show only matching users
  - Verify user count updates to reflect filtered results
  - Clear search field and verify all users are displayed again
- Test email search:
  - Should Enter partial email address of an existing user
  - Verify table filters to show only matching users
  - Clear search field
- Test search with no results:
  - Should Enter text that doesn't match any user data (e.g., "xyz123")
  - Verify table shows "No items found" message
  - Verify user count shows 0 results
  - Clear search field
- Test Case Sensitivity :
  - Should Enter user name in different case (uppercase/lowercase)
  - Verify search works regardless of case
  - Clear search field and verify all users return

## TC 107 - Verify Filter Functionality

### Priority TC 107 : High

- Locate and click "Filters" button on the page
- Verify filter options are displayed
- Test filter by Active status:
  - Select "Active" status filter
  - Verify table shows only users with Active status
  - Verify user count updates to reflect filtered results
  - Clear filter and verify all users are displayed again
- Test filter by Inactive status:
  - Select "Inactive" status filter
  - Verify table shows only users with Inactive status
  - Verify user count updates to reflect filtered results
  - Clear filter and verify all users are displayed again
- Test filter by All status:
  - Select "All" status filter
  - Verify table shows all users regardless of status
  - Verify user count shows total number of users
  - Verify both Active and Inactive users are displayed
  