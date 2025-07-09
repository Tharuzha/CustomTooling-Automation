# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.
- Navigate to <https://cte-dev.iclick.nz/>
- Login as the user in [User Data](..\TestData\UserData.md) file.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/user-roles>

## After Each Test case

- Close the web browser.

## Test Cases

## TC 108 - Verify Navigate to User Roles Page

### Priority TC 108 : High

- Click on "Users & User Roles" dropdown button to expand the menu
- Navigate to User Roles
- Verify Users page opens
- Verify page URL contains "/user-roles"
- Verify page title displays "User Roles"

## TC 109 - Verify Existing User Roles Data

### Priority TC 109 : High

- Navigate to User Roles
- Verify User Roles table is displayed with appropriate columns : Role, Status, Actions
- Verify at least one user role is displayed in the table
- Verify each user role entry contains:
  - Role name information
  - Role status
  - Actions menu (⋮) available
- Verify result count is displayed and shows actual number of user roles

## TC 110 - View User Role Details

### Priority TC 110 : High

- Click on actions (⋮) button for any user role
- Select "View" from the dropdown menu
- Verify navigation to view page with URL containing "/view"
- Verify page title displays "View User Role"
- Verify breadcrumb navigation: Dashboard > Users & User Roles > User Roles > View User Role
- Verify all form fields are disabled and display current role information:
  - User Role field shows role name
  - Role Type dropdown shows selected type (Admin/Staff)
  - Status dropdown shows current status (Active/Inactive)

## TC 111 - Edit User Role Details

### Priority TC 111 : High

- Click on actions (⋮) button for any user role
- Select "Edit" from the dropdown menu
- Verify navigation to edit page with URL containing "/edit"
- Verify page title displays "Edit User Role"
- Verify breadcrumb navigation: Dashboard > Users & User Roles > User Roles > Edit User Role
- Verify all form fields are editable and pre-populated with current role information:
  - User Role text field shows current role name
  - Role Type dropdown shows current type (Admin/Staff) and allows selection
  - Status dropdown shows current status (Active/Inactive) and allows selection
- Make changes to the form fields (modify User Role name, change Role Type)
- Verify that changing Role Type to "Admin" shows detailed permissions matrix with module-specific permissions
- Click "Save" button to save changes
- Verify successful redirect back to User Roles listing page
- Verify updated information is displayed in the table

## TC 112 - Delete User Role

### Priority TC 112 : High

- Note the current number of user roles displayed in the result count
- Click on actions (⋮) button for any user role
- Select "Delete" from the dropdown menu
- Verify confirmation dialog appears with:
  - Title "Are you sure?"
  - Warning message "This action cannot be undone."
  - "Yes, delete it!" button
  - "Cancel" button for cancellation
- Click "Yes, delete it!" to confirm deletion
- Verify success notification appears: "Role successfully deleted!"
- Verify the user role is removed from the table
- Verify result count is decreased by one
- Verify remaining user roles are still displayed correctly

## TC 113 - Cancel Delete User Role

### Priority TC 113 : Medium

- Note the current number of user roles displayed in the result count
- Click on actions (⋮) button for any user role
- Select "Delete" from the dropdown menu
- Verify confirmation dialog appears with proper warning elements
- Click "Cancel" button to cancel the deletion
- Verify confirmation dialog disappears
- Verify the user role remains in the table unchanged
- Verify result count remains the same
- Verify no deletion or changes occurred to the data

## TC 114 - Create New User Role as Role Type : Staff & Inactive Status

### Priority TC 114 : High

- Note the current number of user roles displayed in the result count
- Click on "+User Role" button
- Verify navigation to create page with URL containing "/create"
- Verify page title displays "Add User Role"
- Verify breadcrumb navigation: Dashboard > Users & User Roles > User Roles > Add User Role
- Fill in the form with test data:
  - Enter "TestStaffRole" in User Role field
  - Select "Staff" from Role Type dropdown
  - Select "Inactive" from Status dropdown
- Verify permissions matrix is available for configuration
- Click "Save" button to create the user role
- Verify successful redirect back to User Roles listing page
- Verify new user role "TestStaffRole" appears in the table with:
  - Role name: "TestStaffRole"
  - Status: "Inactive"
  - Actions menu (⋮) available
- Verify result count is increased by one
- Verify the new user role is displayed correctly in the table

## TC 115 - Create New User Role as Role Type : Staff & Active Status

### Priority TC 115 : High

- Note the current number of user roles displayed in the result count
- Click on "+User Role" button
- Verify navigation to create page with URL containing "/create"
- Verify page title displays "Add User Role"
- Verify breadcrumb navigation: Dashboard > Users & User Roles > User Roles > Add User Role
- Fill in the form with test data:
  - Enter "ActiveStaffRole" in User Role field
  - Select "Staff" from Role Type dropdown
  - Select "Active" from Status dropdown
- Verify permissions matrix is available for configuration
- Click "Save" button to create the user role
- Verify successful redirect back to User Roles listing page
- Verify new user role "ActiveStaffRole" appears in the table with:
  - Role name: "ActiveStaffRole"
  - Status: "Active"
  - Actions menu (⋮) available
- Verify result count is increased by one
- Verify the new user role is displayed correctly in the table
- Should Navigate to again Users page with URL containing "/users"
- Click on "+User" button
- Click on Role Dropdown and Verify whether the user role we created is displayed.
