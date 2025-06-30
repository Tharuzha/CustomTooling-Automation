# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/>

## Ater Each Test case

- Close the web browser.

## Test Cases

## TC 001 - Login as a valid user

### Priority : High

- Login as the user in [User Data](CustomTooling-Automation\TestData\UserData.md) file.

## TC 002 - Login as a Valid email and Invalid Password

### Priority : Medium

- Use the valid email from [User Data](CustomTooling-Automation\TestData\UserData.md) file but enter an incorrect password like "WrongPassword123".
- Verify that the login fails and an appropriate error message is displayed.

## TC 003 - Login with Invalid email and Valid Password

### Priority : Medium

- Use an invalid email (e.g., "invalid@email.com") and the valid password from [User Data](CustomTooling-Automation\TestData\UserData.md) file.
- Verify that the login fails and an appropriate error message is displayed. 
