
- ### Splunk Project: Custom App | Dashboards | Advanced Search  

Welcome to my **Splunk Project** repository! This project is part of my ongoing journey to explore and master **Splunk Enterprise**, including onboarding data, building advanced search queries, creating custom apps, and designing comprehensive dashboards.

Throughout this project, I have focused on practical skills to help me in my cybersecurity career, with an emphasis on **real-world applications**, data visualization, and Splunk automation.

## Overview of the Project

### 1. **Splunk App Creation**
In this section of the project, I create a custom app in Splunk to organize the data inputs, searches, and visualizations. Creating a personalized app helps manage complex configurations and enhances the overall Splunk experience.

### 2. **App GUI Icon Upload**
Adding a custom icon to your Splunk app makes the user interface more personalized. I demonstrate how to upload your own icon through the GUI.

### 3. **Dashboard Creation and Configuration**
I walk you through the creation of dashboards from scratch, along with detailed instructions on configuring the dashboard panels and filters for effective data presentation.

### 4. **Panel Creation from Search and Edit**
This part of the project focuses on creating Splunk panels from search results. The goal is to show how to visualize live data and customize the panel appearance.

### 5. **PowerShell Path Setup for Splunk App**
Here, I demonstrate how to use **PowerShell** to find the correct directory path for your Splunk app. This is particularly useful when managing app files and automation scripts.

### 6. **Search and Edit Dashboard Panel**
I explain how to create a panel linked to a search, then edit the search from the panel to refine the data and adjust the visualizations.

---

## Requirements

Before you get started, make sure you have:

- **Splunk Enterprise** installed and running.
- **Splunk Universal Forwarder** to forward data to your Splunk instance.
- **PowerShell** for interacting with Splunk directories and file paths.

## Installation

### 1. **Install Splunk Enterprise**

- Download and install **Splunk Enterprise** by following the official guide.
  [Splunk Download](https://www.splunk.com/en_us/download.html)

### 2. **Install Splunk Universal Forwarder**

- Set up **Splunk Universal Forwarder** to send data from your machine to the main Splunk instance.

### 3. **PowerShell Permissions**

- Make sure **PowerShell** is run as **Administrator** on your machine to perform file path lookups and automation tasks.
 

---

## 📌 Step-by-Step Guide  

### 1️⃣ Splunk App Creation  
Creating a custom app in **Splunk** is essential for organizing configurations and data inputs.  

**Steps:**  
1. Log in to **Splunk**, go to **Settings** > **Apps**.  
2. Click **Create App**.  
3. Fill in the required fields:  
   - **App Name**  
   - **Display Name**  
   - **Description**  
Link (https://dev.splunk.com/enterprise/docs/developapps/createapps)
---

### 2️⃣ App GUI Icon Upload  
Personalizing the UI with a custom icon makes navigation easier.  

**Steps:**  
1. Go to **App Settings**.  
2. Click on **App Icon**.  
3. Upload your **custom icon** (recommended format: `.png` or `.jpg`).  
4. Click **Save** to apply changes.

   Another way To display an icon for your app, do the following:
   
 1. Create the icon files in the following table, in PNG format, preferably with 24-bit transparency
 2. Name the icon files as listed in the table. Filenames are case sensitive. 
 3. Save the icon files to **$SPLUNK_HOME/etc/apps/appname/static/.**
 
    Link (https://dev.splunk.com/enterprise/docs/developapps/createapps)

    ---

### 3️⃣ Dashboard Creation and Configuration  
Dashboards help visualize and analyze data effectively.  

**Steps:**  
1. Navigate to **Dashboards** > **Create New Dashboard**.  
2. Enter a **Dashboard Name** (e.g., *Security Essential*).  
3. Click **Edit** to start adding panels.  
4. Customize panels by configuring search queries and visualizations.  

---

### 4️⃣ Panel Creation from Search & Edit  
A **panel** displays search query results in a Splunk dashboard.  

**Steps:**  
1. Go to **Search** and run a query (example for security event logs):  
 ```splunk
source="WinEventLog:Microsoft-Windows-Sysmon/Operational" EventCode=13
| table _time, ComputerName, TargetObject, Details
```
2. index="security_logs" sourcetype="syslog"
3. Click Save As > Dashboard Panel.
4. Select the dashboard where the panel should be added.
5. Adjust panel settings (e.g., visualization type: table, graph, etc.).

---

### 5️⃣ Powershell Path Setup for Splunk App
Finding the Splunk app directory is crucial for automation and file management.

**Steps:**

1. Open PowerShell as Administrator.
2. Run the following command to get the Splunk installation path 
 
   The app should be on this path on windows :
   C:\Program Files\Splunk\etc\apps\App name :Splunk_Project_App

### 6️⃣ Search & Edit Dashboard Panel ###
You can modify panel searches directly from the dashboard.

**Steps:**

1. Open the Dashboard.
2. Click Edit on the panel you want to modify.
3. Change the search query and update visualization settings.
4. Save changes.

### 7️⃣ Managing Splunk Services: Start/Stop via CMD###
After making changes to Splunk configurations, restart the Splunk service to apply the updates. You can do this by running `splunk restart` in the command line.
### Steps:

📌 **To stop Splunk:**
```bash
splunk stop
```
📌 **To start Splunk:**
```bash
splunk start
```
This is useful for automation and remote management.

## 📸 Project Screenshots
Below are key screenshots from the project:

📌 App Creation
📌 Dashboard Creation
📌 Panel Creation
📌 Search & Edit Panel
📌 Managing Splunk via CMD

🖼️ You can find screenshots in the `/screenshots` directory.
