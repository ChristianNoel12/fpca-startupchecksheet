# FPCA Startup Verification Monitoring System

The FPCA Startup Verification Monitoring System is a web-based manufacturing compliance and traceability platform developed for FPCA (Flexible Printed Circuit Assembly) operations. The system enables operators to complete workstation startup verification checklists, submit records to Firebase Firestore, and provides supervisors with a centralized dashboard for monitoring operational compliance, approval status, audit activities, and historical records.

Key functionalities include MES Startup Checksheet submission, operator and workstation verification, process selection, supervisor approval tracking, real-time Firebase data storage, and CSV export capabilities. All submitted records are stored in the Firebase Firestore `startup_verification` collection and are accessible through the monitoring dashboard.

The Records Dashboard provides real-time visibility of startup verification activities and supports filtering by Operator, Employee ID, Workstation, Process, Shift, Approval Status, Approved By, and Submission Date. Dashboard KPI cards display Total Active Records, Approved Records, Pending Records, and Rejected Records for quick monitoring and management review.

The system incorporates a complete Audit Trail Module that automatically records critical user activities including LOGIN, LOGOUT, SUBMIT_RECORD, EXPORT_CSV, DELETE_RECORD, and DUPLICATE_SUBMISSION events. All audit logs are stored in the Firebase Firestore `audit_logs` collection to support traceability, accountability, internal audits, and customer compliance requirements.

To maintain data integrity and prevent accidental data loss, the system uses a Soft Delete mechanism. Deleted records are never permanently removed from Firebase. Instead, records are updated with audit metadata such as `deleted`, `deletedBy`, `deleteReason`, and `deletedDate`. Deleted records are hidden from the active dashboard but remain available for historical review and audit purposes.

The system also features Deleted Records History Export functionality, allowing supervisors and auditors to generate a dedicated CSV report containing deleted records, deletion reasons, supervisor identification, and deletion timestamps. This ensures complete historical traceability without compromising active production data.

An Audit Logs Export function is available to generate CSV reports of all recorded system activities, providing a chronological trail of user actions for compliance verification and operational investigations.

To improve data quality and prevent duplicate entries, the system implements Duplicate Submission Prevention based on Employee ID, Date, Process, and Shift combinations. Duplicate submissions are automatically blocked and logged within the audit trail for monitoring and investigation.

The platform is designed around FPCA manufacturing requirements, focusing on process traceability, supervisor accountability, audit readiness, historical record retention, operational data integrity, and compliance with manufacturing quality standards.

## Technology Stack

- HTML5
- CSS3
- JavaScript
- Firebase Firestore
- GitHub Pages

## Core Capabilities

- MES Startup Checksheet Submission
- Real-Time Firebase Database Integration
- Compliance Monitoring Dashboard
- KPI Performance Monitoring
- Search and Filter Functions
- Approval Tracking
- Soft Delete Management
- Deleted Records Recovery History
- Audit Trail Logging
- Duplicate Submission Control
- CSV Export Reporting
- Manufacturing Traceability Support

## Developed By

**CNP**
- Process Engineer

### Disclaimer
This project was developed for educational, demonstration, learning, and portfolio purposes. No proprietary company information, customer information, confidential manufacturing data, internal procedures, or restricted business information is included in this repository.

All sample records, workflows, dashboards, and reports are intended solely to demonstrate system functionality and software development capabilities.
