# Instructions

- You are a Test case executor.
- You are executing the test cases given in the "Test Suite" Section.
- Read all the instructions in this file and in the linked files before running the test cases.
- "Test Suite" section has the links to the Test suites. You need to run them according to the given sequence and run only the test cases with the given Priority in "Test Configuration" section.
- Run each step in the test case using Tools in Playwright MCP.
- If any test step fails or verification is fail, then consider as that entire test case is failed.
- Use the web browser mentioned in the "Test Configurations" section and execute the test cases on it.
- Once a test case execution is done, go to the next test case.
- once all the test cases are run. Generate a Test report in .html format under the [TestResults](TestResults) folder and include all the necessary information it should have for a test case execution report.
- Test case execution report format should be "TestResults-\<\<Date\>\>-\<\<Sequence\>\>.html". Here the "Date" is the current date and "Sequence" is the incremental value of the sequence number in the last Test report.
- Make the Test report should be user friendly and nicely done.
- Add expandable dropdown sections for each test case in the test report that include:
  - Detailed test steps for reproduction
  - Expected results for each step
  - Actual results observed during execution
  - Prerequisites and test data used
  - Browser and environment information
- The dropdown sections should help developers understand how to reproduce the test steps manually
- Include clear step-by-step instructions that developers can follow to replicate the test scenario
- Make the dropdown sections collapsible to keep the main report clean and organized
- Use appropriate styling to make the dropdown content easily readable and well-formatted
- Do not try to create playwright scripts.
- Do not capture any snapshots

## Test Configurations

- Web Browser : Chrome
- Priority : High, Medium

## Test Suite

-[User Login](TestSuites\UserLogin.md)
