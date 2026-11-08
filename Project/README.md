# EASYBUDGET

EasyBudget is a lightweight, cross-platform personal finance tracker built with Java and JavaFX. It allows users to log income and expenses, categorize transactions, view financial summaries, and visualize spending through pie charts. The application uses a MySQL database to locally store user credentials and transaction histories.

By group 19:
Cleo Omar
Amaan Jappie
Chulumanco Mkosana
JP Kalenda Tambuy Kitambala
Cleve Ian Williams
Glory Olamide Joseph
Zanele Ester Mangane
Nomagugu Alisa Dube

## FEATURES

* **User Authentication:** Basic login and registration system.

* **Income & Expense Tracking:** Log transactions with specific categories and descriptions.

* **Financial Summary:** Quickly view total income, total expenses, and current balance.

* **Categorized Breakdown:** See exactly where your money is going, grouped by category.

* **Visual Graphs:** Pie charts showing the percentage breakdown of your finances.

* **Cross-Platform Compatibility:** Designed to run seamlessly on both Linux (Zorin OS) and Windows.

## KNOWN LIMITATIONS & SECURITY CONSIDERATIONS

* **No Password Hashing:** Passwords are currently stored in plain text within the database. The login system is **not secure** and should not be used in a production environment or with real, sensitive passwords. It is strictly for local, educational demonstration.

* **Local Only:** This system relies on a local XAMPP database and is not configured for cloud or multi-user network deployment.

## TECH STACK

* **Language:** Java

* **GUI Framework:** JavaFX (Programmatic, no FXML)

* **Database:** MySQL (Hosted locally via XAMPP)

* **Driver:** MySQL Connector/J


## PREREQUISITES

To run and compile this project, you need the following specific software installed on your machine to avoid compatibility issues:

1. **Java Development Kit (JDK) 1.8:**
   *IMPORTANT:* This project requires a JDK that includes JavaFX. (e.g., JDK 1.8.0_111, JDK 1.8.0_431, or BellSoft Liberica JDK 8 Full).

2. **IDE:** NetBeans IDE 8.2 (Newer versions may cause project structure issues).

3. **XAMPP:** Version 8.2.12 is recommended. Used to host the local MySQL database server.

4. **MySQL Connector/J:** The JDBC driver required to connect Java to MySQL (`mysql-connector-j-8.x.x.jar`).


## DIRECTORY MAP inside project folder

* `/build` - Compiled class files.

* `/database` - **Contains the `easybudget.sql` file required for database setup.**

* `/dist` - The distributable executable (.jar) files.

* `/lib` - External libraries and dependencies (e.g., MySQL connector).

* `/nbproject` - NetBeans specific project configuration files.

* `/src` - The raw Java source code files.

* `/test` - Project test files.

* `/README.md` - Current readme file


## SETUP & INSTALLATION

### 1. Strict XAMPP Setup & Module Activation

**CRITICAL INSTALLATION RULE:** When installing XAMPP, it **MUST** be installed directly in your root C: drive: `C:\xampp`. *Do not* install it in the standard "Program Files" directory.

1. Locate the XAMPP Control Panel (`xampp-control.exe`).

2. **CRITICAL:** You MUST right-click the application and select **"Run as administrator"** to ensure proper access rights.

3. Locate the **Apache** and **MySQL** rows in the module table and click the **Start** button for both services.

4. Verify that both modules display a green highlight and show active port numbers (Apache on 80/443, MySQL on 3306).

### 2. Database Configuration (via phpMyAdmin)

1. Open your web browser and navigate to `http://localhost/phpmyadmin` (or click the **Admin** button next to MySQL in XAMPP).

2. In the left-hand navigation panel, click **New** to initiate database creation.

3. Enter `easybudget` as the database name, set the collation drop-down to `utf8mb4_general_ci`, and click **Create**.

4. Select the newly created `easybudget` database from the list on the left side.

5. Click the **Import** tab situated on the top horizontal menu bar.

6. Click **Choose File**, navigate to this project folder, open the `/database` folder, and select the `easybudget.sql` script file.

7. Scroll down and click **Import** (or **Go**).

8. Confirm that the database tree populates with the `users` and `transactions` tables. *(Note: This import includes a default 'LocalProfile' with password 'bypass' for testing).*

### 3. IDE Configuration (Apache NetBeans 8.2)

1. Open NetBeans IDE 8.2.

2. Go to **File > Open Project** and select this entire project folder.

3. Right-click the project -> **Properties** -> **Libraries**.

4. Ensure the Java Platform is set to your JDK 1.8 that includes JavaFX.

5. Click **OK**, then right-click the project and select **Clean and Build**.



## USAGE

Run the `EasyBudget.java` file to launch the application.

* Depending on the current startup flow configured in `EasyBudget.java`, you will either be prompted to register/login, or you will bypass directly to the main menu using the default `LocalProfile` database entry.

* Use the menu buttons to add transactions and view your financial summary. Note that all actions are mirrored in your IDE's console output for easy debugging.


## TEAM DEVELOPMENT NOTES

* **Database Sharing:** If you add new tables or modify the schema, export the database from phpMyAdmin as a `.sql` file, overwrite the one in the `/database` folder, and share it with the team so everyone remains synced.

* **Paths:** Do not use hardcoded local file paths (like `C:\...` or `/home/...`) in the Java code. Rely on relative paths or standard localhost ports (like 3306) to ensure the code runs on both Windows and Linux environments without modification.