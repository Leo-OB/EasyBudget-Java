# Personal Finance Tracker

## Project Overview

The Personal Finance Tracker is a JavaFx-based application developed to help users manage and monitor their personal finances. It allows users to record their income and expenses, organise transactions into categories, and gain insights into their spending habits through visual charts and financial summaries.

## Project Objectives

The objective of the EasyBudget project is to develop a personal finance management application that allows users to track income and expenses, monitor account balances, and analyze spending habits using JavaFX GUI connected to a MySQL database. Designed around a multi-scene layout, the system features user registration and authentication to isolate individual financial records. It enables users to record transactions across structured categories, compute total income, expenses, and net balance alongside overspending alerts, inspect itemized category drop-downs, and visualize financial distribution trends using JavaFX pie charts and text-based percentage bar graphs

## Key Features

- User Security & Data Isolation: Implement registration and login authentication backed by a local MySQL database to store and isolate transaction records per user account.
  
- Transaction Entry: Record income and expense entries with specific amounts, descriptions, and pre-defined category assignments.
  
- Input Validation: Enforce form validation rules to block empty submissions, non-numeric inputs, and negative amount values.

- Balance & Overspending Tracking: Calculate total income, expenses, and net balance in real time, featuring automated warning messages when the user is overspending.

- Data Breakdown & Visualization: Provide financial summaries, itemized category drill-downs, and visual charts via JavaFX pie charts and formatted ASCII bar graphs.

- Duplicate Username Validation: Queries existing MySQL user records before registering new users to prevent duplicate account creation.

- Console & GUI Dual-Logging: Outputs debug messages and operational logs to the terminal while simultaneously updating JavaFX UI feedback banners and text areas.

  

## Technologies Used

- NetBeans IDE: Serves as the Integrated Development Environment (IDE) used to write, structure, compile, and run the JavaFX codebase, as well as debug database connectivity during development.

- XAMPP: Provides the local server stack hosting the MySQL database on localhost:3306 with default local database credentials (root), maintaining the underlying easybudget schema and database lifecycle.

- MySQL: Acts as the relational database management system (RDBMS) running inside XAMPP to persist user account credentials (Users table) and logged income/expense entries (Transactions table).

- JDBC (Java Database Connectivity): Serves as the database API (DriverManager, PreparedStatement, ResultSet) to execute parameterized SQL queries securely, handle multi-user authentication, and pull aggregated financial sums.

- Java Collections API: Utilizes standard collection classes—such as List/ArrayList for managing in-memory transaction lists and Map/LinkedHashMap for grouping and calculating totals per category.

- CSS3 (JavaFX Cascading Style Sheets): Applied through style.css to customize visual aesthetics, featuring dark-mode linear background gradients, button hover/press scale animations, drop shadows, custom scrollbars, and styled pie chart palettes.


## System Design

The EasyBudget application is structured around a modified Model-View-Controller (MVC) architectural pattern, decoupling user interface components from underlying business logic and data storage. At the core of the system is a centralized controller that coordinates interactions between the JavaFX graphical view modules, the database access object, and the MySQL relational database. By separating screen layouts from database logic, the design ensures clean modularity, allowing individual user interface scenes to request and render financial data without managing raw database connections directly.

The EasyBudget class serves as the master application router and window manager, inheriting from JavaFX's Application framework. Upon initialization, it constructs every view module, compiles their corresponding scenes, injects a shared DataStore database instance, and applies global stylesheet configurations from style.css. It maintains state across screen transitions by exposing dedicated routing methods—such as showLogin(), showMenu(), showIncome(), showExpense(), and showGraphs()—that dynamically swap the primary Stage scene. Additionally, it acts as a centralized validator, offering helper routines like amountError() and parseAmount() to enforce strict numerical input validation across all form screens prior to database operations.

The persistence layer is encapsulated within the DataStore Data Access Object (DAO), which handles all database operations using Java Database Connectivity (JDBC). Configured to connect to a MySQL server at jdbc:mysql://localhost:3306/easybudget, DataStore manages multi-user authentication, user registration, transaction recording, and financial summary calculations. Security and session control are maintained through an internal User session object (currentUser), which isolates financial entries by attaching the logged-in user's primary key (user_id) to all database read and write queries. To guard against SQL injection vulnerabilities, all database queries rely on parameterized PreparedStatement executions.

The view layer comprises specialized menu classes (loginMenu, mainMenu, incomeMenu, expenseMenu, financeSummaryMenu, categoryMenu, and graphsMenu), each responsible for constructing discrete JavaFX layout graphs. Input forms collect transaction metadata such as monetary amounts, descriptions, and predefined categories via UI controls like TextField and ComboBox. Visual aesthetics are governed externally by style.css, which enforces a dark-themed visual presentation with linear background gradients, hover and press button scale animations, custom scrollbars, and customized pie chart color schemes.

Data flow within the system culminates in automated financial analysis and dual-format visualization. When users navigate to reporting screens, DataStore executes SQL aggregation queries using SUM and GROUP BY category to compute live account balances, total income, and total expenses. Overspending states are determined dynamically by checking whether total expenses exceed income, triggering UI warnings. Reporting views then process these query outputs: categoryMenu constructs itemized drill-downs listing individual transactions under each category header, while graphsMenu formats the raw totals into both interactive JavaFX PieChart visual nodes and formatted ASCII percentage bar graphs.




## Installation and Setup

Refer to Setup Folder > SetupGuide.md for a visual guide on dependency installation and setup.
Also refer to README.md in Project files

## How to Use

[WIP]


## Group Members
Cput SDN260S Group 19 Members: <br>
Cleo Omar 	<br>
Amaan Jappie 	<br>
Chulumanco Mkosana <br>
JP Kalenda Tambuy Kitambala <br>
Cleve Ian Williams <br>
Glory Olamide Joseph <br>
Zanele Ester Mangane <br>
Nomagugu Alisa Dube <br>
