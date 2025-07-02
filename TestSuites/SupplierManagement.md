# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.
- Navigate to <https://cte-dev.iclick.nz/>
- Login as the user in [User Data](..\TestData\UserData.md) file.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/suppliers>

## After Each Test case

- Close the web browser.

## Test Cases

## TC 007 - Verify Suppliers Page Interface

### Priority TC 007 : High

- Navigate to the suppliers page
- Verify the page title displays "Suppliers"
- Verify the breadcrumb navigation shows "Dashboard > Suppliers"
- Verify the "+ Supplier" button is visible in the top-right corner
- Verify the "Filters" button is present on the left side
- Verify the search box is available with "Search..." placeholder text
- Verify the suppliers table is displayed with the following columns:
  - SUPPLIER (column 1)
  - PHYSICAL ADDRESS (column 2)
  - MAILING ADDRESS (column 3)
  - STATUS (column 4)
  - ACTIONS (column 5)
- Verify that supplier data is loaded and displayed in the table
- Verify that each supplier row shows:
  - Supplier name in the first column
  - Physical address details (when available)
  - Mailing address details (when available)
  - Status indicator showing "Active" in green
  - Actions dropdown menu (three dots) in the last column
- Verify that the interface is responsive and properly formatted
- Verify that all existing suppliers are listed (e.g., "ama edirisighe", "john smith", "test 222", "Innova Pvt", "Universal Supply Chain")

## TC 008 - Verify Add Supplier Form Fields

### Priority TC 008 : High

- Navigate to the suppliers page
- Click on the "+ Supplier" button
- Verify the "Add Supplier" page is loaded
- Verify the page title displays "Add Supplier"
- Verify the breadcrumb navigation shows "Dashboard > Suppliers > Add Supplier"
- Verify the form is divided into the following sections:
  - BASIC INFORMATION section
  - CONTACT DETAILS section
  - PAYMENT DETAILS section
- Verify BASIC INFORMATION section contains:
  - Status dropdown field with "Active" as default selection
  - Supplier Name field with asterisk (*) indicating it's required
- Verify CONTACT DETAILS section contains:
  - Physical Address section with:
    - Address Line 1 text field
    - Address Line 2 text field
    - Address Line 3 text field
  - Mailing Address section with:
    - Address Line 1 text field
    - Address Line 2 text field
    - Address Line 3 text field
  - Phone field with phone icon
  - Fax field with fax icon
  - Email field with email icon
  - MAIN CONTACT subsection with:
    - Name field
    - Phone field with phone icon
    - Email field with email icon
- Verify PAYMENT DETAILS section contains:
  - Payment is Due dropdown with "C.O.D" as default
  - Discount Days field with "30" as default value
  - Balance Due Days field with "30" as default value
  - "Use 31 for EOM" checkbox option
- Verify Note section contains:
  - Large text area for notes
- Verify form action buttons:
  - "Cancel" button (outlined)
  - "Save" button (filled blue)
- Verify all form fields are properly labeled and accessible
- Verify the form layout is responsive and well-organized

## TC 009 - Add New Supplier with Valid Data

### Priority TC 009 : High

- Navigate to the suppliers page
- Click on the "+ Supplier" button
- Verify the "Add Supplier" page is loaded
- Fill in BASIC INFORMATION section:
  - Select "Active" from Status dropdown (if not already selected)
  - Enter "Test Automation Supplier Ltd" in Supplier Name field
- Fill in CONTACT DETAILS section:
  - Physical Address:
    - Enter "123 Business Park Avenue" in Address Line 1
    - Enter "Suite 200" in Address Line 2
    - Enter "Industrial Zone" in Address Line 3
  - Mailing Address:
    - Enter "PO Box 456" in Address Line 1
    - Enter "Business District" in Address Line 2
    - Enter "Commercial Area" in Address Line 3
  - Enter "+1-555-123-4567" in Phone field
  - Enter "+1-555-123-4568" in Fax field
  - Enter "<contact@testautomationsupplier.com>" in Email field
  - MAIN CONTACT section:
    - Enter "John Anderson" in Name field
    - Enter "+1-555-987-6543" in Phone field
    - Enter "<john.anderson@testautomationsupplier.com>" in Email field
- Fill in PAYMENT DETAILS section:
  - Select "In a Given No of Days" from Payment is Due dropdown
  - Enter "45" in Discount Days field
  - Enter "60" in Balance Due Days field
  - Check the "Use 31 for EOM" checkbox
- Fill in Note section:
  - Enter "Test supplier created for automation testing purposes. Specializes in office supplies and equipment." in Note text area
- Click the "Save" button
- Verify successful supplier creation:
  - Verify redirection to suppliers list page
  - Verify success message is displayed (if applicable)
  - Verify the new supplier "Test Automation Supplier Ltd" appears in the suppliers table
  - Verify the new supplier shows "Active" status
  - Verify the supplier data is correctly displayed in the table columns
- Verify supplier details:
  - Click on the newly created supplier's action menu (three dots)
  - Verify options are available for viewing/editing the supplier
  - Verify all entered data is saved correctly in the system

## TC 010 - Set Supplier Status (Active/Inactive)

### Priority TC 010 : Medium

- Navigate to the suppliers page
- Locate an existing supplier in the suppliers table
- Click on the supplier's action menu (three dots)
- Select "Edit" or equivalent option from the dropdown
- Verify the supplier edit page/form is loaded
- Verify the Status dropdown field is available with Active/Inactive options
- Select "Inactive" status if currently "Active" (or "Active" if currently "Inactive")
- Click the "Save" button
- Verify successful status update:
  - Verify redirection to suppliers list page
  - Verify success message is displayed (if applicable)
  - Verify the supplier's status is updated in the suppliers table
  - Verify the status change is correctly reflected (Active/Inactive)
- Verify status persistence:
  - Click on the same supplier's action menu again
  - Select "Edit" or view details
  - Verify the status field shows the updated status value
  - Verify the status information is correctly saved in the system

## TC 011 - Verify Payment Details Dropdown Options

### Priority TC 011 : High

- Navigate to the suppliers page
- Click on the "+ Supplier" button
- Verify the "Add Supplier" page is loaded
- Fill in mandatory BASIC INFORMATION section:
  - Enter "Payment Test Supplier" in Supplier Name field (mandatory field)
- Navigate to PAYMENT DETAILS section
- Verify "Payment is Due" dropdown functionality:
  - Click on the "Payment is Due" dropdown
  - Verify all dropdown options are available:
    - C.O.D
    - Prepaid
    - In a Given No of Days
    - On a Day of the Month
    - No Of Days After EOM
    - Day of Month After EOM
- Test each dropdown option selection:
  - Select "C.O.D" option
  - Verify "C.O.D" is displayed in the dropdown field
  - Select "Prepaid" option
  - Verify "Prepaid" is displayed in the dropdown field
  - Select "In a Given No of Days" option
  - Verify "In a Given No of Days" is displayed in the dropdown field
  - Select "On a Day of the Month" option
  - Verify "On a Day of the Month" is displayed in the dropdown field
  - Select "No Of Days After EOM" option
  - Verify "No Of Days After EOM" is displayed in the dropdown field
  - Select "Day of Month After EOM" option
  - Verify "Day of Month After EOM" is displayed in the dropdown field
- Test supplier creation with dropdown value:
  - Select "Prepaid" from Payment is Due dropdown
  - Enter "15" in Discount Days field
  - Enter "30" in Balance Due Days field
  - Click the "Save" button
- Verify successful supplier creation:
  - Verify redirection to suppliers list page
  - Verify success message is displayed (if applicable)
  - Verify the new supplier "Payment Test Supplier" appears in the suppliers table
- Verify payment details are saved correctly:
  - Click on the newly created supplier's action menu (three dots)
  - Select "Edit" or view details
  - Verify the Payment is Due dropdown shows "Prepaid" as selected
  - Verify Discount Days field shows "15"
  - Verify Balance Due Days field shows "30"
  - Verify all payment details are correctly saved in the system

## TC 012 - View All Suppliers with Pagination

### Priority TC 012 : High

- Navigate to the suppliers page
- Verify the page title displays "Suppliers"
- Verify the suppliers list is loaded and displayed
- Verify supplier list with relevant information is displayed:
  - Verify SUPPLIER column shows supplier names
  - Verify PHYSICAL ADDRESS column shows address details
  - Verify MAILING ADDRESS column shows mailing details
  - Verify STATUS column shows Active/Inactive status
  - Verify ACTIONS column shows action menu (three dots)
- Verify all existing suppliers are visible in the list
- Test pagination functionality (if applicable):
  - Check if pagination controls are present at the bottom of the table
  - Verify current page number is highlighted/selected
  - If multiple pages exist:
    - Click on "Next" button or page number 2
    - Verify navigation to next page works correctly
    - Verify different suppliers are displayed on the new page
    - Verify page number is updated accordingly
    - Click on "Previous" button or page number 1
    - Verify navigation back to previous page works correctly
    - Verify original suppliers are displayed again
- Verify supplier count and total records:
  - Check if total supplier count is displayed
  - Verify the count matches the actual number of suppliers
  - Verify pagination shows correct "showing X of Y records" information
- Test view all functionality:
  - Verify admin can access and view complete supplier list
  - Verify no restrictions on viewing supplier information
  - Verify all supplier data is accessible and readable
  - Verify supplier list loads without errors or timeouts
- Verify list responsiveness:
  - Verify the supplier list is properly formatted
  - Verify all columns are aligned and readable
  - Verify the interface is responsive on different screen sizes

## TC 013 - Search Supplier Functionality

### Priority TC 013 : High

- Navigate to the suppliers page
- Verify the search box is visible with "Search..." placeholder text
- Verify the search box is clickable and functional
- Test basic search functionality:
  - Click on the search box
  - Type "un" in the search field
  - Verify the search is triggered (either automatically or after pressing Enter)
  - Verify matching suppliers appear in the results
  - Verify suppliers containing "un" are displayed (e.g., "Universal Supply Chain")
  - Verify non-matching suppliers are filtered out from the list
- Verify search results display:
  - Verify search results show relevant supplier information
  - Verify SUPPLIER column displays matching supplier names
  - Verify PHYSICAL ADDRESS column shows address details for matching suppliers
  - Verify MAILING ADDRESS column shows mailing details for matching suppliers
  - Verify STATUS column shows Active/Inactive status for matching suppliers
  - Verify ACTIONS column shows action menu (three dots) for matching suppliers
- Test search result count:
  - Verify "Showing X results" or similar count is displayed
  - Verify the count matches the actual number of search results shown
  - Verify the search result count updates correctly
- Test search functionality with different scenarios:
  - Clear the search box and verify all suppliers return to the list
  - Type "Universal" and verify "Universal Supply Chain" appears
  - Type "supply" and verify suppliers with "supply" in the name appear
  - Type a non-existent supplier name and verify "no results" or empty list is shown (e.g., "Johan")
- Verify search behavior:
  - Verify search is case-insensitive (typing "UN", "un", "Un" should work)
  - Verify partial matches work correctly
  - Verify search results update in real-time or after input completion
  - Verify search functionality works without page refresh
- Test search with special characters and edge cases:
  - Type special characters and verify no errors occur
  - Type numbers and verify appropriate results appear
  - Test empty search and verify all suppliers are displayed
- Verify search interaction with other features:
  - Verify search works properly with pagination (if applicable)
  - Verify search results maintain proper formatting and layout
  - Verify action menus work correctly on search results

## TC 014 - Verify Filter Suppliers by Status (Active/Inactive)

### Priority TC 014 : High

- Navigate to the suppliers page
- Verify the "Filters" button is visible on the left side of the page
- Click on the "Filters" button
- Verify the filter panel opens/expands
- Verify the "Active" filter dropdown is available
- Verify the filter dropdown shows "All" as the default selection
- Test filter dropdown options:
  - Click on the "Active" filter dropdown
  - Verify the dropdown shows the following options:
    - All
    - Yes  
    - No
- Test "All" filter option:
  - Select "All" from the dropdown (if not already selected)
  - Verify all suppliers are displayed in the list
  - Verify both Active and Inactive suppliers are shown
  - Verify the supplier count includes all suppliers
- Test "Yes" filter option (Active Suppliers):
  - Select "Yes" from the Active filter dropdown
  - Verify the filter is applied automatically
  - Verify only Active suppliers are displayed in the list
  - Verify all displayed suppliers show "Active" status in the STATUS column
  - Verify Inactive suppliers are filtered out and not visible
  - Verify the supplier count reflects only Active suppliers
  - Verify search results update to show filtered Active suppliers only
- Test "No" filter option (Inactive Suppliers):
  - Select "No" from the Active filter dropdown
  - Verify the filter is applied automatically
  - Verify only Inactive suppliers are displayed in the list
  - Verify all displayed suppliers show "Inactive" status in the STATUS column
  - Verify Active suppliers are filtered out and not visible
  - Verify the supplier count reflects only Inactive suppliers
  - Verify search results update to show filtered Inactive suppliers only
- Test filter functionality with existing suppliers:
  - Verify filter works correctly with the current supplier data
  - Verify suppliers like "Universal Supply Chain", "ama edirisighe", etc. are filtered properly based on their status
  - Verify the filter maintains the table structure and columns
- Test filter reset functionality:
  - After filtering by "Yes" or "No", select "All" again
  - Verify all suppliers (both Active and Inactive) are displayed again
  - Verify the filter reset works correctly
  - Verify the supplier list returns to the original unfiltered state
- Verify filter interaction with other features:
  - Test filter with search functionality:
    - Apply "Yes" filter for Active suppliers
    - Use the search box to search for a specific supplier
    - Verify search results respect the Active filter
    - Verify only Active suppliers matching the search term are shown
  - Test filter with pagination (if applicable):
    - Apply filter and verify pagination updates accordingly
    - Verify page navigation works correctly with filtered results
- Verify filter UI behavior:
  - Verify the filter dropdown shows the selected option correctly
  - Verify the filter state is maintained during page interactions
  - Verify filter selection is clearly indicated in the UI
  - Verify filter controls are accessible and user-friendly
- Test edge cases:
  - If no Active suppliers exist, verify "Yes" filter shows empty list or appropriate message
  - If no Inactive suppliers exist, verify "No" filter shows empty list or appropriate message
  - Verify filter works correctly when suppliers change status
  - Verify filter functionality doesn't cause errors or performance issues

## TC 015 - Edit Existing Supplier Details

### Priority TC 015 : High

- Navigate to the suppliers page
- Verify the suppliers list is loaded and displayed
- Locate an existing supplier in the suppliers table (e.g., "Universal Supply Chain", "ama edirisighe", etc.)
- Click on the supplier's action menu (three dots) in the ACTIONS column
- Verify the action dropdown menu opens with available options
- Click "Edit" option from the dropdown menu
- Verify the "Edit Supplier" page is loaded
- Verify the page title displays "Edit Supplier" or similar
- Verify the breadcrumb navigation shows "Dashboard > Suppliers > Edit Supplier"
- Verify all existing supplier data is pre-populated in the form fields
- Verify the form sections are available:
  - BASIC INFORMATION section
  - CONTACT DETAILS section  
  - PAYMENT DETAILS section
  - Note section
- Test editing BASIC INFORMATION section:
  - Verify the current Status is displayed (Active/Inactive)
  - Verify the current Supplier Name is displayed
  - Update the Supplier Name (e.g., add "- Updated" to the name)
  - Verify the changes can be made in the field
- Test editing CONTACT DETAILS section:
  - Update Physical Address fields:
    - Modify Address Line 1 (e.g., change street number or add "Suite")
    - Update Address Line 2 if needed
    - Update Address Line 3 if needed
  - Update Mailing Address fields:
    - Modify mailing address details
    - Verify changes can be made
  - Update Phone field (e.g., change last few digits)
  - Update Fax field if applicable
  - Update Email field (e.g., change domain or add suffix)
  - Update MAIN CONTACT section:
    - Change contact person Name
    - Update contact Phone number
    - Update contact Email address
- Test editing PAYMENT DETAILS section:
  - Change "Payment is Due" dropdown selection
  - Update "Discount Days" field value
  - Update "Balance Due Days" field value
  - Toggle "Use 31 for EOM" checkbox if applicable
- Test editing Note section:
  - Update the note text area with additional information
  - Verify the text can be modified and saved
- Verify form validation:
  - Ensure required fields (marked with *) cannot be left empty
  - Verify proper field validation is in place
  - Test with invalid data if applicable (e.g., invalid email format)
- Save the changes:
  - Click the "Save" button
  - Verify the save operation is initiated
  - Verify redirection to suppliers list page
  - Verify success message is displayed (if applicable)
- Verify changes are reflected:
  - Locate the updated supplier in the suppliers table
  - Verify the updated supplier name is displayed in the SUPPLIER column
  - Verify any address changes are reflected in PHYSICAL ADDRESS and MAILING ADDRESS columns
  - Verify the STATUS column shows the correct status
  - Verify the supplier data is correctly updated in the table
- Verify data persistence:
  - Click on the updated supplier's action menu (three dots) again
  - Select "Edit" option to view the supplier details
  - Verify all the changes made previously are saved and displayed correctly:
    - Updated Supplier Name
    - Updated contact details (addresses, phone, email)
    - Updated payment details
    - Updated notes
  - Verify no data loss occurred during the edit process
- Test edit permissions:
  - Verify the admin can successfully edit supplier information
  - Verify all form fields are editable and accessible
  - Verify the edit functionality works without errors
- Test edit with different suppliers:
  - Select another supplier from the list
  - Repeat the edit process to ensure consistency
  - Verify the edit functionality works across different supplier records
- Verify table updates:
  - After editing, verify the suppliers table reflects the changes immediately
  - Verify sorting and filtering still work correctly with updated data
  - Verify pagination maintains the updated information
- Test cancel functionality:
  - Start editing a supplier
  - Make some changes to the form
  - Click "Cancel" button (if available)
  - Verify redirection to suppliers list without saving changes
  - Verify the original data remains unchanged

## TC 016 - Delete Supplier Functionality

### Priority TC 016 : High

- Navigate to the suppliers page
- Click on the "+ Supplier" button to create a new supplier for deletion testing
- Verify the "Add Supplier" page is loaded
- Fill in only the mandatory field:
  - Enter "Test Delete Supplier" in Supplier Name field (mandatory field marked with *)
  - Leave all other fields empty (since only supplier name is mandatory)
- Click the "Save" button
- Verify successful supplier creation:
  - Verify redirection to suppliers list page
  - Verify success message is displayed (if applicable)
  - Verify the new supplier "Test Delete Supplier" appears in the suppliers table
  - Verify the new supplier shows "Active" status by default
- Locate the newly created supplier for deletion:
  - Find "Test Delete Supplier" in the suppliers table
  - Verify the supplier is visible in the SUPPLIER column
  - Verify the supplier has an action menu (three dots) in the ACTIONS column
- Access delete functionality:
  - Click on the "Test Delete Supplier" action menu (three dots)
  - Verify the action dropdown menu opens with available options
  - Verify "Delete" option is available in the dropdown menu
  - Click "Delete" option from the dropdown menu
- Verify delete confirmation popup:
  - Verify a popup/modal window appears for delete confirmation
  - Verify the popup contains appropriate delete confirmation message
  - Verify the popup shows the supplier name being deleted
  - Verify the popup has confirmation buttons (e.g., "Cancel" and "Delete" or "Yes" and "No")
  - Verify the popup overlay prevents interaction with the background
- Test delete cancellation:
  - Click "Cancel" or "No" button in the confirmation popup
  - Verify the popup closes without deleting the supplier
  - Verify the supplier "Test Delete Supplier" is still visible in the suppliers table
  - Verify no changes occurred to the supplier list
- Test delete confirmation:
  - Click on the "Test Delete Supplier" action menu (three dots) again
  - Click "Delete" option from the dropdown menu
  - Verify the delete confirmation popup appears again
  - Click "Delete" or "Yes" button to confirm deletion
  - Verify the popup closes after confirmation
- Verify successful deletion:
  - Verify the supplier "Test Delete Supplier" is removed from the suppliers table
  - Verify the supplier no longer appears in the SUPPLIER column
  - Verify the total supplier count is updated (decreased by 1)
  - Verify success message is displayed (if applicable)
  - Verify the suppliers list refreshes properly
- Verify deletion persistence:
  - Refresh the suppliers page (F5 or reload)
  - Verify the deleted supplier "Test Delete Supplier" does not reappear
  - Verify the deletion is permanent and persisted in the database
  - Verify the supplier count remains updated after page refresh
- Test delete functionality with different suppliers:
  - Create another test supplier for deletion testing
  - Enter "Test Delete Supplier 2" in Supplier Name field
  - Save the supplier and verify it appears in the table
  - Repeat the delete process to ensure consistency
  - Verify the delete functionality works across different supplier records
- Verify delete permissions:
  - Verify the admin can successfully access delete functionality
  - Verify the delete option is available in the action menu
  - Verify the delete confirmation process works without errors
- Test edge cases:
  - Verify delete functionality works with suppliers that have minimal data (only name)
  - Verify delete functionality works with suppliers that have complete data
  - Verify the system handles delete operations without causing errors
  - Verify other suppliers in the list are not affected by deletion
- Verify table updates after deletion:
  - After deletion, verify the suppliers table updates immediately
  - Verify pagination adjusts correctly if needed
  - Verify search and filtering still work correctly after deletion
  - Verify the remaining suppliers maintain proper formatting and functionality
