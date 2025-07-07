# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.
- Navigate to <https://cte-dev.iclick.nz/>
- Login as the user in [User Data](..\TestData\UserData.md) file.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/quotes>

## After Each Test case

- Close the web browser.

## Test Cases

## TC 078 - Verify Navigate to Quotes Page

### Priority TC 078 : High

- Navigate to Quotes
- Verify Quotes page opens
- Verify page URL contains "/quotes"
- Verify page title displays "Quotes"
- Verify "+ Quote" button is visible
- Verify "Filters" button is visible
- Verify search box is visible

## TC 079 - Verify View Existing Quotes

### Priority TC 079 : High

- Verify quotes list displays
- Verify table shows quote numbers
- Verify table shows customer type (Regular/One Off)
- Verify table shows customer names
- Verify table shows total amounts
- Verify table shows status badges (DRAFT, APPROVED, WAITING FOR DOCUMENTS, IN NEGOTIATION, VIEWED, SENT)
- Verify table shows actions column with three dots menu
- Verify quotes are displayed in rows
