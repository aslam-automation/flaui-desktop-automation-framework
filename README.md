# FlaUI Desktop Automation Framework

![.NET](https://img.shields.io/badge/.NET-10-blue)
![MSTest](https://img.shields.io/badge/MSTest-Testing-orange)
![FlaUI](https://img.shields.io/badge/FlaUI-UIA3-green)
![C#](https://img.shields.io/badge/C%23-Automation-green)
![Status](https://img.shields.io/badge/Framework-Active-success)

A scalable **Desktop UI Automation Framework** built with **.NET 10, FlaUI UIA3, and MSTest**, following the **Page Object Model (POM)** design pattern.

---

## 🚀 Key Features

- Desktop UI Automation using FlaUI (UIA3)
- Page Object Model (POM) architecture
- Reusable framework components
- Screenshot capture on failure/success
- Extensible reporting support
- Clean separation of Core & Test layers
- Easy integration with CI/CD pipelines

---

## 🛠️ Technology Stack

- **.NET 10** – Application Framework
- **C#** – Programming Language
- **FlaUI UIA3** – Desktop UI Automation Library
- **MSTest** – Test Framework
- **VSTest** – Test Execution Platform
- **Visual Studio 2026** – Development Environment

---

## 🏗️ Framework Architecture

### 📌 High-Level Design

```text
┌──────────────────────────────┐
│ FlaUI.Desktop.Tests          │
│ (Test Layer)                 │
│ - Test Cases                 │
│ - Assertions                 │
└─────────────┬────────────────┘
              │ references
              ▼
┌──────────────────────────────┐
│ FlaUI.Desktop.Core           │
│ (Framework Layer)            │
│ - Pages (POM)                │
│ - Base Classes               │
│ - Helpers                    │
│ - Drivers                    │
│ - Config                     │
└─────────────┬────────────────┘
              │
              ▼
       Desktop Application
```

---

## 📁 Project Structure

```text
FlaUI.Desktop.Automation.Framework
│
├── FlaUI.Desktop.Core
│   ├── Base
│   ├── Pages
│   ├── Helpers
│   ├── Drivers
│   └── Config
│
├── FlaUI.Desktop.Tests
│   ├── Tests
│   └── TestBase
│
└── SampleApplication (Optional)
```

---

## 🔗 Dependency Flow

```text
FlaUI.Desktop.Tests
        ↓ references
FlaUI.Desktop.Core
```

This ensures:
- Clean architecture separation
- Reusable automation components
- Easy scalability for future test expansion

---

## ▶️ Getting Started

### 1️⃣ Clone Repository

```bash
git clone https://github.com/aslam-automation/flaui-desktop-automation-framework.git
cd flaUI.desktop.automation.framework
```

### 2️⃣ Build Solution

```bash
dotnet build
```

### 3️⃣ Run Tests

```bash
dotnet test
```

---

## 📸 Screenshots (Optional)

Add execution or report screenshots here:

```text
/screenshots/test-run.png
/screenshots/report.png
```

Example:

```md
![Test Execution](screenshots/test-run.png)
```

---

## 🔄 CI/CD Pipeline (GitHub Actions)

Create:

```text
.github/workflows/dotnet-tests.yml
```

```yaml
name: .NET Tests

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: windows-latest

    steps:
    - name: Checkout code
      uses: actions/checkout@v4

    - name: Setup .NET
      uses: actions/setup-dotnet@v4
      with:
        dotnet-version: '10.0.x'

    - name: Restore dependencies
      run: dotnet restore

    - name: Build
      run: dotnet build --no-restore

    - name: Run Tests
      run: dotnet test --no-build --verbosity normal
```

---

## 📌 Best Practices Followed

- Page Object Model (POM)
- Separation of Core & Test layers
- Reusable components
- Maintainable folder structure
- CI-ready design

---

## ⚙️ Git Setup

```bash
git init
git add .
git commit -m "initial commit"
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main
```

---

## 👤 Author

**Muhammed Aslam**  
QA Automation Engineer

---

## ⭐ Future Improvements

- HTML test reporting (ExtentReports / Allure)
- Parallel test execution
- Dockerized test runs
- Logging framework integration (Serilog)
