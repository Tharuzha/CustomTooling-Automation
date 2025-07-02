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
