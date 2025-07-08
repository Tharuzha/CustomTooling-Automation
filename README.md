# CustomTooling Automation

This is the repository for Web UI Test Automation for CTE Project with MCP + Playwright and Github Copilot.

MCP (Model Context Protocol) is a framework that allows AI models like Claude to interact with browser automation tools such as Playwright, enabling AI-driven test execution without writing traditional code.

---

## 🚀 Project Overview

CustomTooling-Automation is designed to:
- Enable scalable and maintainable UI testing workflows.
- Integrate with AI models (via MCP) to simplify test execution without traditional scripting.
- Provide structured test data, configurations, and results for the CTE platform.

---

## 🛠 Tech Stack

| Tool          | Purpose                             |
|---------------|-------------------------------------|
| **Playwright** | UI automation framework            |
| **MCP**        | Natural language test interaction   |
| **GitHub Copilot** | AI-assisted development        |
| **HTML**       | Test document samples              |

---

## 📁 Repository Structure

- **TestSuites** — Includes test cases for UI flows  
- **TestData** — Contains user and system data for tests  
- **TestResults** — Holds screenshots and outcome logs  
- **Documentation** — Test strategy PDFs and configuration files  
- **README.md** — Project documentation overview  
- **TestConfiguration.md** — Setup and environment instructions  
---
## 🧪 TestSuites Module Summary

The `TestSuites` folder contains modular Markdown files, each representing test flows or strategies for key modules in the CTE platform.

### 📄 Features

- `CustomerManagement.md` — Covers adding, editing, and deleting customer records  
- `ManageJobStatus.md` — Handles status updates and transitions for jobs  
- `ManageQuoteStatus.md` — Verifies quote status modifications and validations  
- `Quotes.md` — Includes emailing and printing quotes with verification steps  
- `Routing.md` — Documents route planning test cases and validations  
- `StockLocations.md` — Validates creation and editing of stock location entries  
- `SupplierManagement.md` — Automates supplier addition, modification, and removal  
- `SystemSettings.md` — Tests updates to system configurations and field behaviors  
- `Units.md` — Verifies unit search functionality, creation, and deletion  
- `UserLogin.md` — Confirms authentication workflows and error handling  
---

## 🧪 Test Execution Workflow

Test cases are executed based on their assigned **priority levels** and **sequence order** defined in the `TestConfigurations.md` file:

- 🟥 **High**
- 🟧 **Medium**
- 🟩 **Low**

Test cases are executed based on their assigned **priority levels** and **sequence order** defined in the `TestConfigurations.md` file:
Execution order strictly follows the structure in ``.

---

### ⚙️ Execution Steps

1. **Before Each Test Case**  
   📦 Setup the test environment to ensure all dependencies and configurations are ready.

2. **Execute Test Steps**  
   ▶️ Follow the defined steps in each test case using MCP-driven Playwright automation.

3. **After Each Test Case**  
   🧹 Clean up the environment to maintain isolation and prevent state leakage between tests.

4. **Generate Test Report**  
   🧾 Produce an HTML report with detailed test results, including pass/fail statuses and screenshots.

- ✅ This workflow ensures consistency, traceability, and accuracy across all automated test runs.

## ⚙️ Prerequisites

Before running the tests, make sure your environment meets the following requirements:

- ✅ **Playwright MCP**  
  Install and configure the Model Context Protocol (MCP) to enable AI-powered test execution.  
  _Refer to the [Playwright MCP Documentation](#) for setup instructions._

- 🧠 **Visual Studio Code**  
  With GitHub Copilot Chat extension (`v0.11.0` or later) for NLP-based test triggering.

- 🌐 **Browser Support**  
  Chrome or any browser supported by Playwright (as configured in your test settings).

- 📦 **Node.js & npm**  
  Node.js `v16+` and npm package manager.

---

## 🚀 How to Run This Project

Follow these steps to execute your test suite in priority-based order.

### 🔧 Step 1: Clone & Install

# Clone the repo
git clone https://github.com/Tharuzha/CustomTooling-Automation.git
cd CustomTooling-Automation

## ⚙️ Prerequisites

To run this project, ensure the following tools and environments are properly set up:

- **✅ Playwright MCP**  
  Install and configure the Model Context Protocol (MCP) for AI-driven test execution.

- **✅ Visual Studio Code**  
  Make sure GitHub Copilot Chat extension (`v0.11.0` or later) is enabled

- **✅ Browser Support**  
  Chrome or any other browser supported by Playwright.

- **✅ Node.js & npm**  
  Use Node.js version 16 or higher, with npm for dependency management.

---

## 👨‍💻 How to Execute Test Suite via Copilot Chat

Follow these steps to run your automated tests using GitHub Copilot Chat:

### 🧩 Setup

1. **Open** the project in **Visual Studio Code**
2. **Launch** the Copilot Chat panel and select **Claude Sonnet** as your model  ( Claude 3.7 OR Claude 4.0 )
3. **Navigate** to the `TestConfiguration.md` file

### ▶️ Execution

## for simple execution, you can use "Run the Test Suite"
 
4. For advance test executions, You can use this.
   In the Copilot Chat box, enter these commands:
   
   ```text
    You should definitely execute all test cases (TC 067–TC 078) from the Routing.md using Playwright automation.
    Follow the exact test steps and data specified in the test case file. Then generate a report that meets the requirements defined in TestConfiguration.md.

  ```text
  You should definitely execute all test cases (TC 078- TC 092) from the Quotes.md using Playwright automation.
Follow the exact test steps and data specified in the test case file. should do this execute by four test phases.
1. 1st phase: TC 078 - TC 082
2. 2nd phase : TC 083 - TC 086
3. 3rd Phase : TC 087 - TC 089
4. 4th Phase : TC 090 - TC 092
and finally should create a test report according to the requirements of TestConfiguration.md. and included all the test cases ( TC 078 - TC 092)



 
