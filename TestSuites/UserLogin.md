# Instructions

- Run "Before Each Test case" section before running each test case.
- Run "After Each Test case" section after running each test case.

## Before Each Test case

- Navigate to <https://cte-dev.iclick.nz/>

## Ater Each Test case

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

- Enter an email with incorrect format (e.g., "userexample.com" - missing '@' symbol)
- Enter any password (e.g., "password123")
- Click on the login button
- Verify the system shows an appropriate error message for incorrect email format
- Try another invalid email format (e.g., "user@" - missing domain)
- Verify the system correctly validates and rejects the malformed email address
