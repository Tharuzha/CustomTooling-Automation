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

## TC 082 - Verify Filters Functionality (Settings Integration)

### Priority TC 082 : High

#### Step 1: Verify Quote Status Configuration in Settings

- Navigate to Settings > Quote Status
- Verify Quote Status settings page opens
- Record all configured quote statuses from the settings
- Note down all status names (e.g., Draft, Approved, Rejected, etc.)
- Verify each status has proper configuration (name, color, etc.)

#### Step 2: Navigate Back to Quotes Page

- Navigate back to Quotes page
- Verify Quotes page loads successfully

#### Step 3: Verify Filters Functionality

- Click on the "Filters" button
- Verify filters dropdown opens
- Verify "Status" filter section is visible
- Verify Status dropdown shows "All" as default selection
- Click on Status dropdown
- Verify "All" option is available as first option
- Verify all quote status options from Settings > Quote Status appear exactly in the dropdown
- Verify no additional statuses appear that are not configured in Settings
- Verify no configured statuses are missing from the dropdown

#### Step 4: Test Filter Functionality

- Select first available status from dropdown (based on Settings configuration)
- Verify only quotes with that status are displayed
- Verify all visible quotes show the selected status badge
- Verify results count updates to show filtered results only
- Verify "Applied Filters" section appears showing selected status
- Verify "Clear" button is available in applied filters

#### Step 5: Test Second Filter Option

- Select different status from dropdown (based on Settings configuration)
- Verify only quotes with the new status are displayed
- Verify all visible quotes show the new status badge
- Verify results count updates accordingly
- Verify applied filters updates to show the new status

#### Step 6: Reset and Close Filters

- Select "All" from Status dropdown
- Verify all quotes display again regardless of status
- Verify results count returns to original total
- Verify "Applied Filters" section disappears
- Verify Filters button shows no count indicator
- Click outside filters area or close filters
- Verify filters dropdown closes
- Verify table maintains current filter settings

- All quote statuses configured in Settings > Quote Status should appear exactly in Quotes page filters
- No discrepancies between Settings configuration and Filter options
- Filter functionality works correctly for all configured statuses
