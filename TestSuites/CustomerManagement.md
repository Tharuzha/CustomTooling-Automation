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
- Verify all form fields are properly labeled and accessible

