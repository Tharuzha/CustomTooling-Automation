# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/>

## After Each Test case

- Close the web browser.

## Test Cases

## TC 001 - Login as a valid user

### Priority TC 001 : High

- Login as the user in [User Data](..\TestData\UserData.md) file.

## TC 002 - Login as a Valid email and Invalid Password

### Priority TC 002 : Medium

- Use the valid email from [User Data](..\TestData\UserData.md) file but enter an incorrect password like "WrongPassword123".
- Verify that the login fails and an appropriate error message is displayed.

## TC 003 - Login with Invalid email and Valid Password

### Priority TC 003 : Medium

- Use an invalid email (e.g., "<invalid@email.com>") and the valid password from [User Data](..\TestData\UserData.md) file.
- Verify that the login fails and an appropriate error message is displayed.

## TC 004 - Verify Email Format Validation

### Priority TC 004 : Medium

- Enter an email with incorrect format (e.g., "userexample.com" - missing @ symbol)
- Enter any password (e.g., "password123")
- Click on the login button
- Verify that the system accepts the invalid email format without showing HTML5 browser validation
- Verify that form submission is allowed to proceed to the server
- Verify that no client-side validation error message appears for incorrect email format
- Test with another invalid format (e.g., "user@" - missing domain) and verify the same behavior occurs
- Confirm that the application lacks client-side email format validation

## TC 005 - Verify Empty Email Field Validation

### Priority TC 005 : Medium

- Leave the email field empty (clear any existing text)
- Enter any password (e.g., "password123")
- Click on the login button
- Verify the system shows an appropriate error message indicating that email is required
- Verify the login is prevented

## TC 006 - Verify Unauthorized Access Redirect

### Priority TC 006 : High

- Ensure no user is currently logged in (clear browser session/cookies if needed)
- Directly navigate to the dashboard URL: <https://cte-dev.iclick.nz/dashboard>
- Verify that the user is automatically redirected back to the login page
- Verify that the URL changes to "<https://cte-dev.iclick.nz/login>" or similar login URL
- Verify that the login form is displayed instead of the dashboard content
- Ensure unauthorized users cannot access protected dashboard content directly

## TC 093 - Navigate to Forgot Password Page

### Priority TC 093 : Medium

- Navigate to the login page
- Locate the "Forgot Password" link on the login form
- Click on the "Forgot Password" link
- Verify that the user is taken to the Forgot Password page
- Verify that the page URL changes appropriately
- Verify that an email input field is visible on the Forgot Password page

## TC 094 - Submit Valid Email for Reset Link

### Priority TC 094 : Medium

- Navigate to the Forgot Password page
- Enter a valid email address in the email field (e.g., "<tharusha.gunawardhana@leadlanka.lk>")
- Click the "Send Reset Link" button
- Verify that a success message appears confirming the reset link was sent
- Verify that the email field accepts the valid email format
- Verify that the form submission completes successfully

## TC 095 - Submit Empty Email on Forgot Password Page

### Priority TC 095 : Low

- Navigate to the Forgot Password page
- Leave the email field empty
- Click the "Send Reset Link" button
- Verify that an error message appears indicating email is required
- Verify that the reset link is not sent when email field is empty
- Verify that the form prevents submission with empty email field

## TC 096 - Submit Invalid Email for Reset Link

### Priority TC 096 : Medium

- Navigate to the Forgot Password page
- Enter an invalid email address in the email field (e.g., "<invalid@nonexistent.com>")
- Click the "Send Reset Link" button
- Verify that the system shows "We can't find a user with that email address" message
- Verify that no reset link is sent for unregistered email addresses
- Verify that the form handles non-registered emails properly
