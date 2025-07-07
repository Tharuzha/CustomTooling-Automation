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

## TC 084 - Verify Edit Existing Quote Functionality

### Priority TC 084 : High

#### Step 1: Navigate to Edit Quote

- From the Quotes list page, locate a quote with customer data
- Click on the three dots menu to access quote actions
- Select "Edit" from the dropdown menu
- Verify page navigates to Edit Quote page
- Verify page URL contains "/quote" with edit intent or similar edit path
- Verify page title displays "Edit Quote"
- Verify breadcrumb navigation shows: Dashboard > Quotes > Edit Quote

#### Step 2: Modify Quote Fields

- Click on "Customer" dropdown and select Customer "THARUSHA TEST" from the list
- Verify customer selection changes and updates associated fields
- Should set and set his phone number "0713240554".
- Add description text in the "Description" field (e.g., "Updated quote description for testing QUOTES")
- Verify all changes are reflected in the form fields
- Verify form shows modified state

- Click the "Update" button to save changes
- Verify page shows success indication or redirects appropriately
- Verify changes are saved successfully

#### Step 3: Verify Changes Persistence

- Navigate back to the quotes list page
- Locate the same quote that was edited
- Verify the changes are reflected in the quotes list:
- Click to view the quote details again
- Verify all saved changes are persistent

## TC 085 - Verify Cancel Functionality

### Priority TC 085 : Medium

- From the Quotes list page, locate a quote with customer data
- Click on the three dots menu to access quote actions
- Select "Edit" from the dropdown menu
- Make some temporary changes to fields (without saving)
- Change description text in the "Description" field (e.g., "CANCEL")
- Click the "Cancel" button
- Verify page returns to previous state or quotes list
- Verify temporary changes are not saved
- Verify original data remains unchanged

## TC 086 - Add New Quote As Regular Customer

### Priority TC 086 : High

#### Step 1: Adding main details

- Click on "+ Quote" button
- Select Customer Type "Regular"
- Verify "Quote Number" field is automatically generated
- Verify "Quote Number" field displays auto-generated number (e.g., "0017")
- Verify "Quote Number" field is non-editable (frozen/disabled)
- Click on "Status" dropdown
- Verify status dropdown opens with options
- Verify all status options are displayed (Draft, Pending Approval, Approved, Rejected, Expired, Converted to Job, Canceled, Sent, Viewed, In Negotiation, Waiting for Documents)
- Select "Draft" from the status dropdown
- Verify "Draft" status is selected and displayed
- Verify status dropdown closes after selection
- Should click on "Customer" dropdown
- Should select "Jane Smith" from customer dropdown
- Verify customer selection changes to "Jane Smith"
- Verify "Phone" field auto-populates with customer's phone number (e.g., "0761253273")
- Verify "Address" fields auto-populate with customer's address
- If phone or address fields are empty, manually enter the required details:
  - Enter phone number in "Phone" field if not auto-populated
  - Enter address details in "Address" fields if not auto-populated
- Should add Customer P.0 Number (e.g., "22222)
- Should Add description text in the "Description" field (e.g., "We gonna be testing new quote as Regular")
- Verify "QUOTE DETAILS" section is visible
- Verify "Date" field shows current date (e.g., "07/07/2025")
- Verify "Est. Delivery Date" field shows current date (e.g., "07/07/2025")
- Verify "Est. Completion Date" field shows current date (e.g., "07/07/2025")
- Click on "Est. Delivery Date" date picker icon
- Select a future date from the date picker (e.g., "07/15/2025")
- Verify "Est. Delivery Date" field updates with selected date
- Click on "Est. Completion Date" date picker icon
- Select a future date from the date picker (e.g., "07/20/2025")
- Verify "Est. Completion Date" field updates with selected date
- Click on "Finish/Outwork" dropdown
- Select an option from "Finish/Outwork" dropdown
- Verify "Finish/Outwork" selection is displayed
- Click "Save" button
- Verify quote is saved successfully
- Verify the success message after saving
- Verify page remains on edit quote page (does not redirect to quotes list)
- Verify "PARTS" section becomes unlocked/accessible after saving
- Verify "Refresh Data" button is available in PARTS section
- Verify "+ Add Part" button is now visible and enabled
- Verify PARTS table shows columns: PART TYPE, PART NO, DESCRIPTION, VERSION, QTY, UNIT, UNIT PRICE, TOTAL, ACTION
- Verify "No items found, try to broaden your search" message appears in PARTS section
- Verify Sub Total shows "$0.00"
- Verify GST (16%) shows "$0.00"
- Verify Total shows "$0.00"
- Verify "FILE ATTACHMENTS" section becomes unlocked/accessible after saving
- Verify "Refresh Data" button is available in FILE ATTACHMENTS section
- Verify "+ File" button is now visible and enabled
- Verify FILE ATTACHMENTS table shows columns: NAME, DATE, FILE, ACTION
- Verify "No items found, try to broaden your search" message appears in FILE ATTACHMENTS section

#### Step 2: Modifying Parts Section as normally

- Click On "+ Add Part" Button
- Verify "Add Part" dialog opens
- Verify "One Off" checkbox is unchecked (do not tick "One Off")
- Click on "Part Code" dropdown
- Select "PN-0006" from the part code dropdown
- Verify part code selection changes to "PN-0006"
- Verify "Part Description" field auto-populates with "PN-0006 Description"
- Enter quantity "20" in the "Qty" field
- Verify quantity field shows "20"
- Enter "v2" in the "Version" field (if available)
- Click on "Units" dropdown
- Select a unit from the Units dropdown
- Verify unit selection is displayed
- Enter "30" in the "Unit Price" field
- Verify unit price field shows "30"
- Click "Save" button
- Verify part is added successfully
- Verify part appears in the PARTS table
- Verify part row shows: PN-0006, Description, v2, 20, selected unit, 30, calculated total
- Verify Sub Total updates to reflect the new part total
- Verify GST (16%) updates based on new subtotal
- Verify Total updates to include GST

#### Step 3: Add another Part as One off

- Click On "+ Add Part" Button
- Verify "Add Part" dialog opens
- Tick the "One Off" checkbox
- Verify "One Off" checkbox is checked
- Verify "Part Code" field becomes empty text input (not dropdown)
- Manually enter "CUSTOM-001" in the "Part Code" field
- Verify part code field shows "CUSTOM-001"
- Manually enter "Custom One-Off Part Description" in the "Part Description" field
- Verify part description field shows entered text
- Enter quantity "15" in the "Qty" field
- Verify quantity field shows "15"
- Enter "v1" in the "Version" field
- Verify version field shows "v1"
- Click on "Units" dropdown
- Select a unit from the Units dropdown
- Verify unit selection is displayed
- Enter "45" in the "Unit Price" field
- Verify unit price field shows "45"
- Click "Save" button
- Verify one-off part is added successfully
- Verify part appears in the PARTS table
- Verify part row shows: One Off type, CUSTOM-001, Custom description, v1, 15, selected unit, 45, calculated total
- Verify Sub Total updates to include both parts
- Verify GST (16%) updates based on new subtotal
- Verify Total updates to include all parts with GST

#### Step 4: Verify FILE ATTACHMENTS Section Functionality

- Click On "+ File" Button
- Verify "Add File" dialog opens
- Verify "Name" field is empty and ready for input
- Enter "test file pdf" in the "Name" field
- Verify name field shows "test file pdf"
- Verify "Date" field shows current date (e.g., "2025-07-07")
- Verify "Date" field is pre-populated with current date
- Verify file upload area displays "Upload a file or drag and drop"
- Verify file upload area shows "PDF, DOCX up to 5MB" file type restrictions
- Click on the cloud upload icon/area
- Verify file chooser dialog opens
- Select and upload a PDF file (e.g., test document)
- Verify uploaded file appears in the upload area
- Verify uploaded file name is displayed (e.g., "test-document-428595-quote_attachment.pdf")
- Verify uploaded file shows proper file extension and format
- Click "Save" button
- Verify file attachment is saved successfully
- Verify success message appears: "Quote Attachment created successfully!"
- Verify "Add File" dialog closes after successful save
- Verify file appears in the FILE ATTACHMENTS table
- Verify file attachment row shows: "test file pdf", current date, PDF filename, action menu
- Verify FILE ATTACHMENTS table displays all required columns:
  - NAME column shows "test file pdf"
  - DATE column shows "2025-07-07"
  - FILE column shows clickable PDF link "test-document-428595-quote_attachment.pdf"
  - ACTION column shows "⋮" menu button for file actions
- Verify PDF file link is clickable for download/view access
- Verify FILE ATTACHMENTS section no longer shows "No items found" message
- Verify file attachment is properly integrated with the quote
- Verify "Refresh Data" button is available for refreshing attachment list

## TC 087 - Add New Quote As One Off Customer

### Priority TC 087 : High

#### Step 1: Adding main details for One Off

- Click on "+ Quote" button
- Select Customer Type "One-Off"
- Verify "Quote Number" field is automatically generated
- Verify "Quote Number" field displays auto-generated number (e.g., "0017")
- Verify "Quote Number" field is non-editable (frozen/disabled)
- Click on "Status" dropdown
- Verify status dropdown opens with options
- Verify all status options are displayed (Draft, Pending Approval, Approved, Rejected, Expired, Converted to Job, Canceled, Sent, Viewed, In Negotiation, Waiting for Documents)
- Select "Draft" from the status dropdown
- Verify "Draft" status is selected and displayed
- Verify status dropdown closes after selection
- Should click on "Customer" dropdown
- Should Add on Customer Name field (e.g., "Test OneOff")
- Should add on Customer P.0 Number (e.g., "33333)
- Should add on phone number field (e.g., "0781212122")
- Should Add description text in the "Description" field (e.g., "We gonna be testing new quote as One Off")
- Verify "QUOTE DETAILS" section is visible
- Verify "Date" field shows current date (e.g., "07/07/2025")
- Verify "Est. Delivery Date" field shows current date (e.g., "07/07/2025")
- Verify "Est. Completion Date" field shows current date (e.g., "07/07/2025")
- Click on "Est. Delivery Date" date picker icon
- Select a future date from the date picker (e.g., "07/20/2025")
- Verify "Est. Delivery Date" field updates with selected date
- Click on "Est. Completion Date" date picker icon
- Select a future date from the date picker (e.g., "07/25/2025")
- Verify "Est. Completion Date" field updates with selected date
- Click on "Finish/Outwork" dropdown
- Select an option from "Finish/Outwork" dropdown
- Verify "Finish/Outwork" selection is displayed
- Click "Save" button
- Verify quote is saved successfully
- Verify the success message after saving
- Verify page remains on edit quote page (does not redirect to quotes list)
- Verify "PARTS" section becomes unlocked/accessible after saving
- Verify "Refresh Data" button is available in PARTS section
- Verify "+ Add Part" button is now visible and enabled
- Verify PARTS table shows columns: PART TYPE, PART NO, DESCRIPTION, VERSION, QTY, UNIT, UNIT PRICE, TOTAL, ACTION
- Verify "No items found, try to broaden your search" message appears in PARTS section
- Verify Sub Total shows "$0.00"
- Verify GST (16%) shows "$0.00"
- Verify Total shows "$0.00"
- Verify "FILE ATTACHMENTS" section becomes unlocked/accessible after saving
- Verify "Refresh Data" button is available in FILE ATTACHMENTS section
- Verify "+ File" button is now visible and enabled
- Verify FILE ATTACHMENTS table shows columns: NAME, DATE, FILE, ACTION
- Verify "No items found, try to broaden your search" message appears in FILE ATTACHMENTS section

#### Step 2: Modifying Parts Section as One off customer

- Click On "+ Add Part" Button
- Verify "Add Part" dialog opens
- Verify "One Off" checkbox is unchecked (do not tick "One Off")
- Click on "Part Code" dropdown
- Select "PN-0006" from the part code dropdown
- Verify part code selection changes to "PN-0006"
- Verify "Part Description" field auto-populates with "PN-0006 Description"
- Enter quantity "20" in the "Qty" field
- Verify quantity field shows "20"
- Enter "v2" in the "Version" field (if available)
- Click on "Units" dropdown
- Select a unit from the Units dropdown
- Verify unit selection is displayed
- Enter "30" in the "Unit Price" field
- Verify unit price field shows "30"
- Click "Save" button
- Verify part is added successfully
- Verify part appears in the PARTS table
- Verify part row shows: PN-0006, Description, v2, 20, selected unit, 30, calculated total
- Verify Sub Total updates to reflect the new part total
- Verify GST (16%) updates based on new subtotal
- Verify Total updates to include GST

#### Step 3: Add another Part as One off in One Off Customer

- Click On "+ Add Part" Button
- Verify "Add Part" dialog opens
- Tick the "One Off" checkbox
- Verify "One Off" checkbox is checked
- Verify "Part Code" field becomes empty text input (not dropdown)
- Manually enter "CUSTOM-001" in the "Part Code" field
- Verify part code field shows "CUSTOM-001"
- Manually enter "Custom One-Off Part Description" in the "Part Description" field
- Verify part description field shows entered text
- Enter quantity "15" in the "Qty" field
- Verify quantity field shows "15"
- Enter "v1" in the "Version" field
- Verify version field shows "v1"
- Click on "Units" dropdown
- Select a unit from the Units dropdown
- Verify unit selection is displayed
- Enter "45" in the "Unit Price" field
- Verify unit price field shows "45"
- Click "Save" button
- Verify one-off part is added successfully
- Verify part appears in the PARTS table
- Verify part row shows: One Off type, CUSTOM-001, Custom description, v1, 15, selected unit, 45, calculated total
- Verify Sub Total updates to include both parts
- Verify GST (16%) updates based on new subtotal
- Verify Total updates to include all parts with GST

## TC 088 - Delete Quote and Verify

### Priority TC 088 : High

#### Step 1: Navigate to Quotes List

- Navigate to Quotes page
- Verify Quotes page loads successfully
- Verify quotes list displays with existing quotes
- Record the total number of quotes displayed (e.g., "Showing 1 to 10 of 17 results")
- Select a quote to delete from the list (choose any quote that is not critical for other tests)

#### Step 2: Access Delete Functionality

- Locate the target older quote in the quotes list
- Click on the action menu button (⋮) for the selected quote
- Verify action dropdown menu opens
- Verify menu contains options: "View", "Edit", "Delete"
- Click on "Delete" option
- Verify "Delete" button is clickable and accessible

#### Step 3: Confirm Deletion

- Verify confirmation dialog appears with title "Are you sure?"
- Verify dialog displays warning message "This action cannot be undone."
- Verify dialog contains two buttons: "Yes, delete it!" and "Cancel"
- Click "Yes, delete it!" button to confirm deletion
- Verify confirmation dialog closes after clicking confirm

#### Step 4: Verify Successful Deletion

- Verify success message appears: "Quote successfully deleted!"
- Verify success notification is displayed prominently
- Verify the deleted quote is no longer visible in the quotes list
- Verify the quote row has been completely removed from the table
- Verify total results count has decreased by 1 (e.g., from "17 results" to "16 results")
- Verify page automatically updates to show remaining quotes
- Verify pagination updates correctly if applicable

#### Step 5: Verify Data Persistence

- Refresh the page manually
- Verify the deleted quote remains absent from the list
- Verify total count remains updated after page refresh

## TC 089 - Convert Quote to a Job

### Priority TC 089 : High

#### Step 1: Navigate to Edit Quote page

- Navigate to Quotes page
- Verify Quotes page loads successfully
- From the Quotes list page, locate a quote with customer data (e.g., quote 0016)
- Click on the action menu button (⋮) for the selected quote
- Verify action dropdown menu opens
- Verify menu contains options: "View", "Edit", "Delete"
- Click on "Edit" option
- Verify page navigates to Edit Quote page
- Verify page URL contains "/quote" with edit intent
- Verify page title displays "Edit Quote"
- Verify breadcrumb navigation shows: Dashboard > Quotes > Edit Quote

#### Step 2: Initiate Quote to Job Conversion

- Verify "Make into Job" button is visible in the top action bar
- Click on "Make into Job" button
- Verify confirmation dialog appears
- Verify dialog title displays "Are you sure?"
- Verify dialog shows warning icon (!)
- Verify dialog displays message: "Do you want to convert this quote into a job?"
- Verify dialog contains two buttons: "Yes, convert it!" and "Cancel"

#### Step 3: Confirm Quote to Job Conversion

- Click "Yes, convert it!" button to confirm conversion
- Verify confirmation dialog closes after clicking confirm
- Verify page navigation occurs (URL changes from quote to job)

#### Step 4: Verify Successful Conversion to Job

- Verify page URL changes to "/job/" format (e.g., contains job UUID)
- Verify page title changes from "Edit Quote" to "Edit Job"
- Verify breadcrumb navigation updates to: Dashboard > Jobs > Edit Job
- Verify job number is auto-generated and displayed (e.g., "0032")
- Verify job number field is non-editable/disabled

#### Step 5: Verify Job Details Section

- Verify "Job Details" section is visible
- Verify "Job No" field displays auto-generated job number and is disabled
- Verify "Job Status" dropdown shows "Pending" as default selection
- Verify "Job Type" dropdown shows "MTO - Make To Order" as default selection
- Verify "Order Date" field shows current date (e.g., "2025-07-07")
- Verify "Delivery Date" field inherits value from quote's estimated delivery date

## TC 090 - Duplicate an Existing Quote

### Priority TC 090 : High

#### Step 1: Navigate to Edit Quote Page

- Navigate to Quotes page
- Verify Quotes page loads successfully
- From the Quotes list page, locate an existing quote with complete data (e.g., quote 0018)
- Click on the action menu button (⋮) for the selected quote
- Verify action dropdown menu opens
- Verify menu contains options: "View", "Edit", "Delete"
- Click on "Edit" option
- Verify page navigates to Edit Quote page
- Verify page URL contains "/quote" with edit intent
- Verify page title displays "Edit Quote"
- Verify breadcrumb navigation shows: Dashboard > Quotes > Edit Quote

#### Step 2: Initiate Quote Duplication

- Verify "Copy Quote" button is visible in the top action bar
- Click on "Copy Quote" button
- Verify confirmation dialog appears
- Verify dialog title displays "Are you sure?"
- Verify dialog shows warning icon (!)
- Verify dialog displays message: "Do you want to copy this quote into new?"
- Verify dialog contains two buttons: "Yes, copy it!" and "Cancel"

#### Step 3: Confirm Quote Duplication

- Click "Yes, copy it!" button to confirm duplication
- Verify confirmation dialog closes after clicking confirm
- Verify page navigation occurs (URL changes to new quote)

#### Step 4: Verify Successful Quote Duplication

- Verify page URL changes to new quote format (e.g., contains new quote UUID)
- Verify page title remains "Edit Quote"
- Verify breadcrumb navigation shows: Dashboard > Quotes > Edit Quote
- Verify new quote number is auto-generated and displayed (e.g., "0020")
- Verify new quote number field is non-editable/disabled
- Verify new quote number is different from original quote number

#### Step 5: Verify Customer Information is Copied

- Verify "Customer Information" section displays copied data
- Verify "Type" field shows same customer type as original (e.g., "Regular")
- Verify "Status" field shows same status as original (e.g., "Draft")
- Verify "Customer" field shows same customer name as original (e.g., "Jane Smith")
- Verify "Customer P.O Number" field shows same value as original
- Verify "Phone" field shows same phone number as original
- Verify "Address" fields show same address as original
- Verify "Description" field shows same description as original

#### Step 6: Verify Quote Details are Copied

- Verify "Quote Details" section displays copied data
- Verify "Date" field shows current date (e.g., "2025-07-07")
- Verify "Est. Delivery Date" field shows same date as original
- Verify "Est. Completion Date" field shows same date as original
- Verify "Finish/Outwork" field shows same selection as original
- Verify "Fabrication" checkbox shows same state as original

#### Step 7: Verify Parts Section is Copied

- Verify "Parts" section displays all copied parts data
- Verify parts table shows same number of parts as original
- Verify each part row contains same data as original:
  - Part Type (Regular/One-Off)
  - Part No (e.g., PN-0006, CUSTOM-001)
  - Description
  - Version
  - Quantity
  - Unit
  - Unit Price
  - Total
- Verify "Sub Total" shows same amount as original (e.g., "$1,275.00")
- Verify "GST (16%)" shows same amount as original (e.g., "$204.00")
- Verify "Total" shows same amount as original (e.g., "$1,479.00")

#### Step 8: Verify File Attachments are Copied

- Verify "File Attachments" section displays copied attachments
- Verify file attachments table shows same files as original
- Verify each attachment row contains:
  - Same file name as original
  - Date may show "N/A" for copied files
  - Same file link (may reference original quote storage)
  - Action menu available

#### Step 9: Navigate Back and Verify Both Quotes Exist

- Navigate back to Quotes page
- Verify Quotes page loads successfully
- Verify quotes list displays both original and copied quotes
- Verify total results count has increased by 1
- Verify original quote is still present in the list
- Verify new copied quote appears in the list (usually at the top)
- Verify both quotes show identical data except for quote numbers:
  - Original quote: same quote number as before (e.g., "0018")
  - Copied quote: new quote number (e.g., "0020")
  - Both quotes: same customer, total amount, and status

## TC 091 - Email Quote to Customer

### Priority TC 091 : High

#### Step 1: Navigate to quotes

- Navigate to Quotes page
- Verify Quotes page loads successfully
- From the Quotes list page, locate an existing quote with customer data (e.g., quote 0020)
- Click on the action menu button (⋮) for the selected quote
- Verify action dropdown menu opens
- Verify menu contains options: "View", "Edit", "Delete"
- Click on "Edit" option
- Verify page navigates to Edit Quote page
- Verify page title displays "Edit Quote"

#### Step 2: Verify Email Quote Button

- Verify "Email Quote" button is visible in the top action bar
- Verify "Email Quote" button is clickable and enabled
- Verify button displays email icon and "Email Quote" text
- Verify button appears alongside other action buttons (Make into Job, Copy Quote, Print)

## TC 092: Print Existing Quote

### Priority TC 092 : High

#### Step 1: Navigate to quotes for cheking Print

- Navigate to Quotes page
- Verify Quotes page loads successfully
- From the Quotes list page, locate an existing quote with customer data (e.g., quote 0020)
- Click on the action menu button (⋮) for the selected quote
- Verify action dropdown menu opens
- Verify menu contains options: "View", "Edit", "Delete"
- Click on "Edit" option
- Verify page navigates to Edit Quote page
- Verify page title displays "Edit Quote"

#### Step 2: Verify and Click Print Button

- Verify "Print" button is visible in the top action bar
- Verify "Print" button is clickable and enabled
- Verify button displays print icon and "Print" text
- Verify button appears alongside other action buttons (Make into Job, Copy Quote, Email Quote)
- Click on "Print" button
- Verify print dialog opens or PDF is generated
- Verify the generated document contains all quote details:
  - Quote number
  - Customer information
  - Quote date
  - Parts list with quantities and prices
  - Total amount
  - Company branding/header
