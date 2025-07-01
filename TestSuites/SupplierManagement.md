# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.
- Navigate to <https://cte-dev.iclick.nz/>
- Login as the user in [User Data](..\TestData\UserData.md) file.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/suppliers>

## Ater Each Test case

- Close the web browser.

## Test Cases

## TC 001 - Verify Suppliers Page Interface

### Priority TC 001 : High

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

## TC 002 - Verify Add Supplier Form Fields

### Priority TC 002 : High

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
