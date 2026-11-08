# How to install dependencies and run Easy Budget

## Required Dependencies

### 1. Java JDK 1.8.0 (Choose ONE of the following options)

**Option 1: JDK 1.8.0_111 (64-bit Windows)**

* https://archive.org/download/jdk-8u111-nb-8_2

**Option 2: JDK 1.8.0_431 (64-bit Windows)**

* https://www.oracle.com/java/technologies/javase/javase8u211-later-archive-downloads.html
* Under the heading "Java SE Development Kit 8u431", download the 64-bit Windows installer:
  `jdk-8u431-windows-x64.exe`

### 2. NetBeans IDE 8.2

* https://archive.org/download/jdk-8u111-nb-8_2
* Download the 64-bit Windows version (this contains both NetBeans IDE 8.2 and JDK 1.8.0_111).

### 3. XAMPP

* https://sourceforge.net/projects/xampp/files/XAMPP%20Windows/8.2.12/
* Download the installer titled:
  `xampp-windows-x64-8.2.12-0-VS16-installer.exe`

---

## Guide to Install Required JDK Versions and NetBeans Version

Follow the installation instructions for the selected JDK version and NetBeans IDE 8.2.

Make sure that the JDK is installed correctly before opening the EasyBudget project in NetBeans.

---

## XAMPP Installation and Setup

Follow the steps below to install XAMPP, configure MySQL and import the EasyBudget database.

### Step 1: Search for XAMPP

![Step 1 - Search for XAMPP](../Imgs/Xampp%20Screenshots/1.SearchXampp.png)

### Step 2: Open More Downloads

![Step 2 - More Downloads](../Imgs/Xampp%20Screenshots/2.MoreDownloads.png)

### Step 3: Select XAMPP for Your Operating System

![Step 3 - Choose XAMPP for OS](../Imgs/Xampp%20Screenshots/3.ChooseXamppForOS.png)

### Step 4: Find and Select XAMPP Version 8.2.12

![Step 4 - Select XAMPP 8.2.12](../Imgs/Xampp%20Screenshots/4.SearchSelect8.2.12.png)

### Step 5: Download the XAMPP Installer

![Step 5 - XAMPP Installer](../Imgs/Xampp%20Screenshots/5.XamppInstaller.png)

### Step 6: Start XAMPP Setup

![Step 6 - XAMPP Setup](../Imgs/Xampp%20Screenshots/6.SetupXampp.png)

### Step 7: Continue with the Installation

![Step 7 - Click Next](../Imgs/Xampp%20Screenshots/7.Next.png)

### Step 8: Choose the Installation Location

The recommended installation location used in this guide is:

`C:\xampp`

![Step 8 - Installation Location](../Imgs/Xampp%20Screenshots/8.InstallationLocation.png)

### Step 9: Complete the Installation

![Step 9 - Installation](../Imgs/Xampp%20Screenshots/9.Installation.png)

### Step 10: Run XAMPP as Administrator

![Step 10 - Run as Administrator](../Imgs/Xampp%20Screenshots/10RunAsAdmin.png)

### Step 11: Verify the XAMPP Control Panel

![Step 11 - Correct Display](../Imgs/Xampp%20Screenshots/11.CorrectDisplay.png)

### Step 12: Start MySQL and Access phpMyAdmin

![Step 12 - Admin MySQL](../Imgs/Xampp%20Screenshots/12.AdminMysql.png)

### Step 13: Create the EasyBudget Database

Create a new database named `easybudget` in phpMyAdmin.

![Step 13 - Create Database](../Imgs/Xampp%20Screenshots/13.CreateDatabase.png)

### Step 14: Open the Import Tab

Select the newly created database and navigate to the Import tab.

![Step 14 - Import](../Imgs/Xampp%20Screenshots/14.Import.png)

### Step 15: Choose the EasyBudget SQL File

Locate and select the `easybudget.sql` file included in the project's database folder.

![Step 15 - Choose File](../Imgs/Xampp%20Screenshots/15.ChooseFile.png)

### Step 16: Import the SQL File

Click the Import/Go button to execute the SQL file and create the required database tables.

![Step 16 - Import SQL](../Imgs/Xampp%20Screenshots/16.ImportSql.png)

### Step 17: Verify the Database

Confirm that the EasyBudget database and its tables have been successfully created in phpMyAdmin.

![Step 17 - Verify Database](../Imgs/Xampp%20Screenshots/17.Verify.png)

---
