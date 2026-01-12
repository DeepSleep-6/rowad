# Rowad Medical Services - Calls Dashboard

A serverless dashboard application for managing hospital outreach, tracking medical device interactions, and visualizing call outcomes.

## Project Description

This Single Page Application (SPA) provides a graphical interface for the Rowad Medical Services team to interact with their outreach database. It replaces direct spreadsheet manipulation with a secure, user-friendly UI that enforces data integrity and provides real-time analytics.

## Features

### Dashboard & Visualization
* **Kanban-Style Card View:** Visualizes hospital status with binary color coding (Gold for interacted, Grey for pending).
* **Data Table:** High-density view for quick scanning and sorting.
* **Analytics:** Real-time charts via Chart.js displaying:
    * Call Outcomes (Quote Requested, Call Later, Not Interested).
    * Satisfaction Metrics (Satisfied vs. Unsatisfied vs. Neutral).

### Data Management
* **CRUD Operations:** Full read/write capabilities for hospital records, including contact details, notes, and tagging.
* **Search & Filtering:** Client-side filtering by geographical direction and multi-field text search.
* **Export:** Client-side generation of CSV exports for external reporting.

### Access Control
* **Role-Based Access:** * **Admin/Editor:** Full write access.
    * **Public/Viewer:** Read-only access.
* **Authentication:** Integration with Google Identity Services (OAuth 2.0).

## Technology Stack

* **Frontend:** HTML5, CSS3, JavaScript (ES6+).
* **Backend:** Google Apps Script (Web App deployment).
* **Database:** Google Sheets.
* **Dependencies:** Chart.js, FontAwesome.

## Configuration & Setup

### Prerequisites
1.  **Google Sheet:** A structured spreadsheet containing hospital data.
2.  **Google Cloud Platform:** A project configured with an OAuth 2.0 Client ID.

## Usage
Open `index.html` in any modern web browser. The application handles authentication via the "Sign In" button in the navigation bar.
