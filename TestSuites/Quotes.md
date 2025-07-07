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

## TC 080 - Verify Search Functionality by Quote Number

### Priority TC 080 : High

- Click on the search box
- Should Enter "0016" in the search box
- Verify search filters the results as user types
- Verify only quote "0016" is displayed
- Verify other quotes are hidden from the list
- Verify "Showing 1 results" appears at bottom
- Verify quote details match (Jane Smith, Regular, 170.00, DRAFT status)
- Should Clear the search box
- Verify all quotes display again
- Verify results count returns to original total

## TC 081 - Verify Search Functionality by Customer Name

### Priority TC 081 : High

- Click on the search box
- Should Enter "Jane" in the search box
- Verify search filters the results as user types
- Verify only quotes with customer name containing "Jane" are displayed
- Verify other quotes are hidden from the list
- Verify all displayed quotes show "Jane Smith" as customer name
- Verify results count updates to show filtered results only
- Should Clear the search box
- Verify all quotes display again
- Verify results count returns to original total
- Next should enter "noname"
- Verify No results from that name
- Verify displayed message "No items found, try to broaden your search"

## TC 082 - Verify Filters Functionality

### Priority TC 082 : High

- Click on the "Filters" button
- Verify filters dropdown opens
- Verify "Status" filter section is visible
- Verify Status dropdown shows "All" as default selection
- Click on Status dropdown
- Verify all status options are available:
  - All
  - Approved
  - Canceled
  - Converted to Job
  - Draft
  - Expired
  - In Negotiation
  - Pending Approval
  - Rejected
  - Sent
  - Viewed
  - Waiting for Documents
- Select "Draft" from Status dropdown
- Verify only quotes with "Draft" status are displayed
- Verify all visible quotes show "Draft" status badge
- Verify results count updates to show filtered results only
- Select "Approved" from Status dropdown
- Verify only quotes with "Approved" status are displayed
- Verify all visible quotes show "Approved" status badge
- Verify results count updates accordingly
- Select "All" from Status dropdown
- Verify all quotes display again regardless of status
- Verify results count returns to original total
- Click outside filters area or close filters
- Verify filters dropdown closes
- Verify table maintains current filter settings
