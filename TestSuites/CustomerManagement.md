# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.
- Navigate to <https://cte-dev.iclick.nz/>
- Login as the user in [User Data](..\TestData\UserData.md) file.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/customers>

## After Each Test case

- Close the web browser.

## Test Cases

## TC 018 - Verify Customers Page Interface

### Priority TC 018 : High

- Navigate to the customers page
- Verify the page title displays "Customers"
- Verify the breadcrumb navigation shows "Dashboard > Customers"
- Verify the "+ Customer" button is visible in the top-right corner
- Verify the "Filters" button is present on the left side
- Verify the search box is available with "Search..." placeholder text
- Verify the customers table is displayed with the following columns:
  - CUSTOMER (column 1)
  - PHYSICAL ADDRESS (column 2)
  - MAILING ADDRESS (column 3)
  - CATEGORY (column 4)
  - STATUS (column 5)
  - ACTIONS (column 6)
- Verify that customer data is loaded and displayed in the table
- Verify that each customer row shows:
  - Customer name in the first column
  - Physical address details (when available)
  - Mailing address details (when available)
  - Category information (e.g., "Flues", "Power")
  - Status indicator showing "Active" in green
  - Actions dropdown menu (three dots) in the last column
- Verify that all existing customers are listed (e.g., "THARUSHA TEST", "vindiiiiii dd", "fwergerger", "eeeferteftr", "Mike John", "Retail Co.")
- Verify pagination shows "Showing 1 to 10 of 15 results"
- Verify pagination controls are present at the bottom

## TC 019 - Verify Add Customer Form Fields

### Priority TC 019 : High

- Navigate to the customers page
- Click on the "+ Customer" button
- Verify the "Add Customer" page is loaded
- Verify the page title displays "Add Customer"
- Verify the breadcrumb navigation shows "Dashboard > Customers > Add Customer"
- Verify the form sections are displayed:
  - BASIC INFORMATION section
  - CONTACT DETAILS section
  - ADDITIONAL DETAILS section
  - PAYMENT DETAILS section
- Verify BASIC INFORMATION section contains:
  - Status dropdown field with "Active" as default selection
  - Customer field with asterisk (*) indicating it's required
- Verify CONTACT DETAILS section contains:
  - Physical Address section with Address Line 1, 2, 3 fields
  - Mailing Address section with Address Line 1, 2, 3 fields
  - Phone field with phone icon
  - Fax field with fax icon
  - Email field with email icon
  - MAIN CONTACT subsection with Name, Phone, Email fields
- Verify ADDITIONAL DETAILS section contains:
  - Category dropdown field with "-" as default
  - "Show Deliveries on Invoice" checkbox option
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
- Verify all form fields are properly labeled and accessible.

## TC 020 - Add New Customer with Valid Data

### Priority TC 020 : High

**MUST FOLLOW EXACT TEST STEPS:**

- Execute each test case using the EXACT data specified in the test steps
- DO NOT use generic or assumed data

- Navigate to the customers page
- Click on the "+ Customer" button
- Verify the "Add Customer" page is loaded
- Fill in BASIC INFORMATION section:
  - Select "Active" from Status dropdown (if not already selected)
  - Enter "Test Automation Tharusha" in Customer field
- Fill in CONTACT DETAILS section:
  - Physical Address:
    - Enter "456 Business Center Road" in Address Line 1
    - Enter "Floor 3, Suite 300" in Address Line 2
    - Enter "Tech District" in Address Line 3
  - Mailing Address:
    - Enter "PO Box 789" in Address Line 1
    - Enter "Commercial Hub" in Address Line 2
    - Enter "Business Zone" in Address Line 3
  - Enter "+1-555-456-7890" in Phone field
  - Enter "+1-555-456-7891" in Fax field
  - Enter "<contact@testautomationcustomer.com>" in Email field
  - MAIN CONTACT section:
    - Enter "Sarah Wilson" in Name field
    - Enter "+1-555-123-9876" in Phone field
    - Enter "<sarah.wilson@testautomationcustomer.com>" in Email field
- Fill in ADDITIONAL DETAILS section:
  - Select "Power" from Category dropdown
  - Tick the "Show Deliveries on Invoice" checkbox
- Fill in PAYMENT DETAILS section:
  - Select "In a Given No of Days" from Payment is Due dropdown
  - Enter "15" in Discount Days field
  - Enter "45" in Balance Due Days field
- Fill in Note section:
  - Enter "Test customer created for automation testing purposes. Specializes in power equipment and solutions." in Note text area
- Click the "Save" button
- Verify successful customer creation:
  - Verify redirection to customers list page
  - Verify success message is displayed (if applicable)
  - Verify the new customer "Test Automation Customer Ltd" appears in the customers table
  - Verify the new customer shows "Active" status
  - Verify the customer data is correctly displayed in the table columns

## TC 021 - Verify Mandatory Fields Validation

### Priority TC 021 : High

- Navigate to the customers page
- Click on the "+ Customer" button
- Verify the "Add Customer" page is loaded
- Attempt to create customer without filling mandatory fields:
  - Leave the Customer field empty (required field marked with *)
- Fill in CONTACT DETAILS section:
  - Physical Address:
    - Enter "456 Walasmulla" in Address Line 1
    - Enter "Floor 3, Suite 300" in Address Line 2
    - Enter "Tech District" in Address Line 3
- Click the "Save" button
- Verify mandatory field validation:
  - Verify error message appears for the Customer field
  - Verify the form does not submit
  - Verify customer is not created
  - Verify user remains on the Add Customer page

## TC 022 - Verify Complete Form Validation with All Fields Empty

### Priority TC 022 : High

- Navigate to the customers page
- Click on the "+ Customer" button
- Verify the "Add Customer" page is loaded
- Attempt to create customer with all fields empty:
  - Leave ALL form fields empty (including Customer field marked with *)
  - Do not fill any field in BASIC INFORMATION section
  - Do not fill any field in CONTACT DETAILS section
  - Do not fill any field in ADDITIONAL DETAILS section
  - Do not fill any field in PAYMENT DETAILS section
  - Do not fill any field in Note section
- Click the "Save" button
- Verify complete form validation:
  - Verify error message appears for all mandatory fields
  - Verify the form does not submit
  - Verify customer is not created
  - Verify user remains on the Add Customer page
  - Verify no partial customer record is created in the system

## TC 023 - Verify Admin Can View Full Customer List

### Priority TC 023 : High

- Navigate to the customers page
- Verify the page loads successfully and displays the customers table
- Verify admin access to customer data:
  - Verify all existing customers are displayed in the table
  - Verify customer data is visible and readable
- Verify customer list completeness:
  - Count the total number of customers displayed
  - Verify pagination shows correct total count (e.g., "Showing 1 to 10 of X results")
  - Verify all customer records are accessible through pagination
- Verify customer information visibility:
  - Verify customer names are displayed in the CUSTOMER column
  - Verify physical addresses are displayed (when available)
  - Verify mailing addresses are displayed (when available)
  - Verify categories are displayed (e.g., "Flues", "Power", "-")
  - Verify status information is displayed (e.g., "Active")
  - Verify actions menu is available for each customer
- Verify admin can navigate through all customers:
  - If pagination exists, verify admin can access all pages
  - Verify admin can view customers on different pages

## TC 024 - Verify Edit Customer Details

### Priority TC 024 : High

**MUST FOLLOW EXACT TEST STEPS:**

- Execute each test case using the EXACT data specified in the test steps
- DO NOT use generic or assumed data

- Navigate to the customers page
- Verify the customers table is displayed with existing customers
- Select a customer to edit:
  - Locate an existing customer in the table (e.g., "Test Automation Tharusha")
  - Click on the actions menu (three dots) for the selected customer
  - Click on "Edit" or equivalent action from the dropdown menu
- Verify the "Edit Customer" page is loaded:
  - Verify the page title displays "Edit Customer" or similar
  - Verify the breadcrumb navigation shows "Dashboard > Customers > Edit Customer"
  - Verify all form fields are pre-populated with existing customer data
- Modify customer details in BASIC INFORMATION section:
  - Change Customer name to "Updated Test Automation Customer Ltd"
  - Verify Status dropdown shows current value and can be modified
- Modify customer details in CONTACT DETAILS section:
  - Physical Address:
    - Change Address Line 1 to "789 Updated Business Center Road"
    - Change Address Line 2 to "Floor 5, Suite 500"
    - Change Address Line 3 to "Updated Tech District"
  - Mailing Address:
    - Change Address Line 1 to "PO Box 999"
    - Change Address Line 2 to "Updated Commercial Hub"
    - Change Address Line 3 to "Updated Business Zone"
  - Change Phone to "+1-555-999-8888"
  - Change Fax to "+1-555-999-8889"
  - Change Email to "<updated.contact@testautomationcustomer.com>"
  - MAIN CONTACT section:
    - Change Name to "Updated Sarah Wilson"
    - Change Phone to "+1-555-999-7777"
    - Change Email to "<updated.sarah.wilson@testautomationcustomer.com>"
- Modify customer details in ADDITIONAL DETAILS section:
  - Change Category from "Power" to "Flues"
  - Toggle the "Show Deliveries on Invoice" checkbox (if previously checked, uncheck it)
- Modify customer details in PAYMENT DETAILS section:
  - Change Payment is Due to "Prepaid"
  - Change Discount Days to "20"
  - Change Balance Due Days to "60"
- Modify Note section:
  - Change Note to "Updated test customer for automation testing purposes. Now specializes in flue systems and solutions."
- Click the "Save" button
- Verify successful customer update:
  - Verify redirection to customers list page
  - Verify success message is displayed (if applicable)
  - Verify the updated customer "Updated Test Automation Customer Ltd" appears in the customers table
  - Verify the updated customer data is correctly displayed in the table columns
- Verify changes are persisted:
  - Click on the actions menu for the updated customer
  - Click on "Edit" to view the customer details again
  - Verify all modified fields display the updated values
  