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

- Navigate to the customers page
- Click on the "+ Customer" button
- Verify the "Add Customer" page is loaded
- Fill in BASIC INFORMATION section:
  - Select "Active" from Status dropdown (if not already selected)
  - Enter "Test Automation Customer Ltd" in Customer field
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
  - Leave other mandatory fields empty if any
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
  - Verify no access restrictions prevent viewing customer information
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
  - Verify no customers are hidden or inaccessible
- Verify search functionality (if available):
  - Verify admin can search for specific customers
  - Verify search results display correctly
  - Verify search does not restrict admin access
- Verify admin permissions:
  - Verify no "Access Denied" or permission errors occur
  - Verify admin can view all customer details without restrictions
  - Verify full administrative access to customer management section

