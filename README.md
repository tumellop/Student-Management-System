# Student Management System

A comprehensive web application designed to manage student data, built using **ASP.NET Core MVC** and **Razor Pages**. This project demonstrates enterprise-level software design patterns, specifically **Onion Architecture**, to ensure loose coupling and high maintainability.

## 🚀 Key Features

* **Onion Layer Architecture:** The application is structured into distinct layers (Domain, Service, Infrastructure, Web) to strictly enforce the **Separation of Concerns (SoC)** principle.
* **Dynamic Database Creation:** Utilizes **Entity Framework Core** Code-First Migrations to dynamically generate the database schema and associated DataTables upon initialization.
* **Secure Authentication & Authorization:** Full user management system implemented with ASP.NET Core Identity (Registration, Login, Role-based access).
* **Hybrid Web Approach:** Combines standard **MVC Controllers** with **Razor Pages** for optimized UI rendering.
* **Web API:** Includes a RESTful API layer for external data consumption.

## 🛠️ Tech Stack

* **Framework:** ASP.NET Core 8.0 (or your specific version)
* **Pattern:** MVC (Model-View-Controller) & Razor Pages
* **ORM:** Entity Framework Core
* **Database:** SQL Server (LocalDB/Express)
* **Architecture:** Onion (Clean) Architecture
* **Frontend:** HTML5, CSS3, Bootstrap, JavaScript

## 📂 Architecture Overview

The solution is divided into concentric layers to isolate the core business logic from external dependencies:

1.  **Domain Layer:** Contains enterprise entities and database models (No dependencies).
2.  **Service Layer:** Holds interfaces and business logic.
3.  **Infrastructure Layer:** Implements data access, EF Core DbContext, and migrations.
4.  **Presentation Layer:** The ASP.NET Core Web Project (MVC/Razor/API).

## ⚙️ Getting Started

Follow these steps to set up the project locally.

### Prerequisites
* [Visual Studio 2026](https://visualstudio.microsoft.com/) (or 2022) with the "ASP.NET and web development" workload.
* .NET SDK.
* SQL Server Express or LocalDB.

### Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/tumellop/Student-Management-System.git](https://github.com/tumellop/Student-Management-System.git)
    ```

2.  **Open the Solution**
    Open `StudentManagementSystem.sln` in Visual Studio.

3.  **Configure Database**
    Update the connection string in `appsettings.json` within the Presentation layer to match your local SQL Server instance.

4.  **Apply Migrations**
    Open the **Package Manager Console** (Tools > NuGet Package Manager > Package Manager Console).
    Run the following command to dynamically create the database and tables:
    ```powershell
    Update-Database
    ```

5.  **Run the Application**
    Press `F5` or click the "Start" button in Visual Studio to launch the application.

## 🤝 Contributing

Contributions are welcome! Please fork the repository and create a pull request for any feature enhancements or bug fixes.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
