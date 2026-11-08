# How to Install dependencies and run EasyBudget

## First Install Required Dependencies

The project requires Java JDK 1.8.0_XXX, NetBeans IDE 8.2 and XAMPP.

**Important:** There are two options for installing Java and NetBeans:

- **Option 1:** Install the combined NetBeans IDE 8.2 and JDK 1.8.0_111 installer. This installs both together.
- **Option 2:** Install JDK 1.8.0_431 separately, then install NetBeans IDE 8.2 separately.

Choose ONE option. You do not need to install both JDK versions.
<br>
<br>
<br>

### 1. Combined NetBeans 8.2 and JDK installer: (Option 1)

**Download:**

* https://archive.org/download/jdk-8u111-nb-8_2
* Download the 64-bit Windows installer, which includes both NetBeans IDE 8.2 and JDK 1.8.0_111.

**Installation instructions:**

1. Search for NetBeans IDE 8.2 and JDK 1.8.0_111 in your brower, click the website or url shown below.

   ![Search for NetBeans](../Imgs/Netbeans%20IDE%208.2%20and%20JDK%201.8.0_111%20Screenshots/1.SearchVer.png)

2. Download and save the combined installer.

   ![Save installer](../Imgs/Netbeans%20IDE%208.2%20and%20JDK%201.8.0_111%20Screenshots/2.SaveNetbeansAndJDK.png)

3. After installation, Netbeans should automatically connect to version JDK 1.8.0_111, if prompted choose that version

<br>
<br>
<br>

### 2. Java JDK 1.8.0_431 (Option 2)

**Download:**

* https://www.oracle.com/java/technologies/javase/javase8u211-later-archive-downloads.html
* Under the heading "Java SE Development Kit 8u431", download:
  `jdk-8u431-windows-x64.exe`

**Installation instructions:**

1. Search for JDK 8u431 on the Oracle website.

   ![Search for JDK](../Imgs/JDK%201.8.0_431%20Screenshots/1.SearchJdk.png)

2. Scroll down to locate the JDK 8u431 downloads under the heading "Java SE Development Kit 8u431".

   ![Locate JDK download](../Imgs/JDK%201.8.0_431%20Screenshots/2.Scroll.png)

3. Download the 64-bit Windows installer `jdk-8u431-windows-x64.exe`.

   ![Download JDK](../Imgs/JDK%201.8.0_431%20Screenshots/3.Download.png)

4. Install Netbeans 8.2 using same link in Option 1, during installation, when prompted to choose JDK Java file, choose 1.8.0_431


---


## XAMPP Installation and Setup

Follow the steps below to install XAMPP, configure MySQL and import the EasyBudget database.
* https://sourceforge.net/projects/xampp/files/XAMPP%20Windows/8.2.12/
* Download the installer:
  `xampp-windows-x64-8.2.12-0-VS16-installer.exe`

### Step 1: Search for XAMPP in your brower, click following url/website:

![Step 1 - Search for XAMPP](../Imgs/Xampp%20Screenshots/1.SearchXampp.png)

### Step 2: Open More Downloads

![Step 2 - More Downloads](../Imgs/Xampp%20Screenshots/2.MoreDownloads.png)

### Step 3: Select XAMPP for Your Operating System, Windows in this case

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

`C:\xampp` !!This Location MUST be used, will cause errors if installed in programfiles or different location!!

![Step 8 - Installation Location](../Imgs/Xampp%20Screenshots/8.InstallationLocation.png)

### Step 9: Complete the Installation

![Step 9 - Installation](../Imgs/Xampp%20Screenshots/9.Installation.png)

### Step 10: Run XAMPP as Administrator
Xampp MUST be ran as Administrator, either by right clicking the control pane .exe in files or searching up the application, right clicking and running as Administrator

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
EasyBudget>database, Also refer to Projects readme.md file found in project folder for where to accesss and find easybudget.sql

![Step 15 - Choose File](../Imgs/Xampp%20Screenshots/15.ChooseFile.png)

### Step 16: Import the SQL File

Click the Import/Go button to execute the SQL file and create the required database tables.

![Step 16 - Import SQL](../Imgs/Xampp%20Screenshots/16.ImportSql.png)

### Step 17: Verify the Database

Confirm that the EasyBudget database and its tables have been successfully created in phpMyAdmin.

![Step 17 - Verify Database](../Imgs/Xampp%20Screenshots/17.Verify.png)

---
