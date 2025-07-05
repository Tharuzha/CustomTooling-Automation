# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.
- Navigate to <https://cte-dev.iclick.nz/>
- Login as the user in [User Data](..\TestData\UserData.md) file.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/system>

## After Each Test case

- Close the web browser.

## Test Cases

## TC 027 - Verify Navigate to System Settings Page

### Priority TC 027 : High

- Navigate to System Settings
- Verify System Settings page opens
- Verify page URL contains "/system"
- Verify page title displays "System Settings"

## TC 028 - Verify System Settings Page Interface

### Priority TC 028 : High

- Navigate to the system settings page
- Verify the page title displays "Settings - System"
- Verify the breadcrumb navigation shows "Dashboard > Settings > System"
- Verify the "FINANCIAL SETTINGS" section is displayed with the following fields:
  - Buy/Sell Premium input field is present and contains numeric value
  - Purchase Margin input field is present and contains numeric value
  - Labor Cost input field is present and contains numeric value
  - Material Cost Percentage input field is present and displays "%" symbol
  - Invoice Cost Percentage input field is present and displays "%" symbol
  - GST Rate input field is present and displays "%" symbol
- Verify the "EMAIL SETTINGS" section is displayed with the following fields:
  - Send Email To input field is present and contains email address
  - CC Emails field is present with existing email tags (if any)
  - CC Emails field shows helper text "(Use a comma to separate multiple email addresses.)"
  - Type email input field is present with appropriate placeholder text
- Verify the "TIME MANAGEMENT SETTINGS" section is displayed with the following fields:
  - Stop/Start Time Allowance input field is present and contains numeric value
  - Staff Clock Minutes input field is present and contains numeric value
  - Clock Grace Minutes input field is present and contains numeric value
- Verify the "AUTOMATIC LUNCH BREAK SETTINGS" section is displayed with the following fields:
  - Lunch Start Time input field is present and contains time value
  - Lunch Stop Time input field is present and contains time value
  - Automatic Lunch Break checkbox is present and functional
- Verify the "Save" button is present at the bottom of the page
- Verify all input fields are editable and functional
- Verify all sections are properly organized and labeled
- Verify the page layout is responsive and user-friendly

## TC 029 - Update all system setting fields and verify

### Priority TC 029 : High

- Update Buy/Sell Premium field with new value
- Update Purchase Margin field with new value
- Update Labor Cost field with new value
- Update Material Cost Percentage field with new value
- Update Invoice Cost Percentage field with new value
- Update GST Rate field with new value
- Update Send Email To field with new email address
- Add new email to CC Emails field (e.g., "<tharu@email.lk>")
- Type this Email on CC Emails fields and after type a comma
- Update Stop/Start Time Allowance field with new value
- Update Staff Clock Minutes field with new value
- Update Clock Grace Minutes field with new value
- Click on Lunch Start Time field to open time picker
- Select new time using the time picker for Lunch Start Time
- Click on Lunch Stop Time field to open time picker  
- Select new time using the time picker for Lunch Stop Time
- Toggle Automatic Lunch Break checkbox
- Click Save button
- Verify success message appears
- Refresh the page
- Verify all updated values are saved and displayed correctly
