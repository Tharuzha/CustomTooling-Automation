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

## TC 083 - Verify View Quote Details (Read-Only Mode)

### Priority TC 083 : High

#### Step 1: Navigate to View Quote

- From the Quotes list page, locate a quote with customer data
- Click on the quote number or three dots menu to access quote details
- Select "View" or click directly on quote to open quote details page
- Verify page navigates to View Quote page
- Verify page URL contains "/quotes/view" or similar quote view path
- Verify page title displays "View Quote"

#### Step 2: Verify Customer Information Section (Read-Only)

- Verify "CUSTOMER INFORMATION" section is visible
- Verify "Type" field displays customer type (Regular/One Off) and is read-only
- Verify "Customer" field shows selected customer name and is non-editable
- Verify customer dropdown is disabled/read-only (cannot be changed)
- Verify "Address" fields display complete customer address in read-only format:
  - Street address line 1 (non-editable)
  - Street address line 2 (non-editable if applicable)
  - City, State, ZIP code (non-editable)
- Verify "Description" field displays quote description and is read-only

#### Step 3: Verify Quote Header Information (Read-Only)

- Verify "Status" field displays current quote status and is read-only
- Verify status matches the status shown in quotes list
- Verify "Quote Number" field displays unique quote identifier and is read-only
- Verify quote number cannot be edited or modified
- Verify "Customer P.O Number" field displays value and is non-editable
- Verify "Phone" field displays customer contact number and is read-only

#### Step 4: Verify Quote Details Section (Read-Only)

- Verify "QUOTE DETAILS" section is visible
- Verify "Date" field displays quote creation/issue date and is read-only
- Verify "Est. Delivery Date" field shows estimated delivery and is non-editable
- Verify "Est. Completion Date" field shows estimated completion and is non-editable
- Verify date fields use proper date format (MM/DD/YYYY) and cannot be modified
- Verify "Finish/Outwork" field displays selected value and is read-only
- Verify "Fabrication" section displays information and is non-editable

#### Step 5: Verify Parts Section (Display Only)

- Verify "PARTS" section is displayed
- Verify "Refresh Data" button is available for data refresh only
- Verify parts table contains the following columns in read-only format:
  - PART TYPE (display only)
  - PART NO (display only)
  - DESCRIPTION (display only)
  - VERSION (display only)
  - QTY (display only)
  - UNIT (display only)
  - UNIT PRICE (display only)
  - TOTAL (display only)
  - ACTION (view/display actions only)
- Verify parts data is displayed but cannot be edited
- Verify each part row shows complete information in read-only format
- Verify "Sub Total" displays sum of all part totals (calculated, non-editable)
- Verify "GST (16%)" displays calculated tax amount (read-only)
- Verify "Total" displays final amount including GST (calculated, non-editable)

#### Step 6: Verify File Attachments Section (Display Only)

- Verify "FILE ATTACHMENTS" section is displayed
- Verify "Refresh Data" button is available for refreshing attachment list only
- Verify attachments table contains columns in read-only format:
  - NAME (display only)
  - DATE (display only)
  - FILE (display only with download/view capability)
  - ACTION (view/download actions only)
- Verify file attachments are listed if any exist but cannot be modified
- Verify attachment names are clickable for viewing/downloading only
- Verify file types are properly displayed (e.g., PDF links) for viewing only

#### Step 7: Verify Navigation and Breadcrumbs

- Verify breadcrumb navigation shows: Dashboard > Quotes > View Quote
- Verify breadcrumb links are functional
- Verify user can navigate back to quotes list
