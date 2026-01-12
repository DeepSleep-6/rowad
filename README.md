# Rowad Medical Services - Calls Dashboard

This project is a centralized dashboard designed to track, manage, and visualize outreach calls to hospitals. It replaces raw spreadsheet data with a user-friendly interface, allowing the team to monitor call outcomes, satisfaction ratings, and device details in real-time.

## What It Does

* **Visual Tracking:** Displays hospitals as cards.
    * **Gold Border:** Indicates interaction has occurred (Call Later, Quote Requested, etc.).
    * **Grey Border:** Indicates the call is still "Pending."
* **Data Visualization:** Includes charts to instantly view:
    * Call Outcomes (excluding pending calls for better scale).
    * Satisfaction Rates (Satisfied vs. Unsatisfied vs. Neutral).
* **Search & Filter:** Instantly filter hospitals by "Direction" or search by name, city, or contact number.
* **Editing:** Authorized users (Admins/Editors) can click any card to update contact info, status, notes, and tags directly.
* **Export:** One-click download of the entire database to CSV.

## Technical Overview

The application runs on a serverless architecture, using Google services to handle the backend and database, ensuring zero hosting costs and high availability.

* **Frontend:** A single HTML file (`index.html`) containing all CSS styling and JavaScript logic.
* **Database:** Google Sheets.
* **Backend API:** Google Apps Script (GAS) acts as the bridge between the frontend and the spreadsheet.
* **Authentication:** Google Sign-In (OAuth 2.0) handles user identity and access control.

## Setup Instructions

If you need to deploy this dashboard from scratch, follow these steps:

### 1. The Database (Google Sheets)
Create a new Google Sheet with these exact headers in the first row:
`Hospital Name`, `Region`, `City`, `Direction`, `Device`, `Surfacide SN`, `AccuFIT SN`, `Surfacide Username`, `Contact`, `Contact Mobile Number`, `Satisfaction`, `Status`, `Tags`, `Notes`.

### 2. The Backend (Apps Script)
1.  In your Google Sheet, go to **Extensions > Apps Script**.
2.  Paste the backend code (provided separately).
3.  Deploy as a **Web App**.
    * *Execute as:* Me.
    * *Who has access:* Anyone. (Security is handled by the Token in the frontend).
4.  Copy the generated **Web App URL**.

### 3. The Frontend Configuration
Open `index.html` and update the following variables:
1.  **SCRIPT_URL:** Paste your Web App URL here.
2.  **data-client_id:** Paste your Google Cloud OAuth Client ID here.

## Usage Rights

This software is developed for the internal use of Rowad Medical Services. Access to write/edit data is restricted to authorized email accounts.
