# petalynx
⌢瀠瑥污獳•਍# ITE412_SIA2_Lynxs_Petalynx

Hello, We are the Team Lynxs of BSIT IV F3

Our Title is "Petalynx"

# Team Members:
Project Leader- Arjay Basconcillo
Project Presenter-Kieth U. Mendizabal
Project Documenter-Trecia mae. M Gandia
Project Diagrammer- Mike Jayson C. Ordonio

This system is a e-commerce platform for flowers. So our stakeholders are the customers
flower shop owner and also the florist. On this platform, we will integrate different
functionalities popular in e-commerce platform like order, inventory, status updates and extraction 
of reports.


Clone a GitHub repository to your local machine using these steps:

Get the Repository URL

Go to the repository page on GitHub.

Click the green Code button above the file list.

Select your protocol (HTTPS or SSH) and click the Copy icon next to the URL.

Open Your Terminal

Windows: Open Command Prompt, PowerShell, or Git Bash.

macOS / Linux: Open Terminal.

Navigate to Your Target Directory

Change into the folder where you want to save the project:
Run the Clone Command

Execute the git clone command followed by the copied URL:

Enter the Cloned Repository

Move into the newly created project folder to start working:

# High-Level System Overview
1. Major Modules / Subsystems
User Management Module
Handles user registration, authentication, profile management, and account security for customers, shop owners, and administrators.
Flower Catalog Management Module
Allows shop owners to upload, update, and manage flower products available in their stores. Customers can browse and search available flowers.
Order and Payment Management Module
Processes customer orders, tracks order status, records transactions, and manages payment information.
Administrative Management Module
Enables administrators to manage users, monitor transactions, generate reports, and oversee system operations.

2. External Systems / Interfaces
Firebase Authentication
Used for secure user login and authentication.
Firebase Firestore Database
Stores customer data, flower listings, orders, payment records, and system information.
Payment Gateway (Future Integration)
Can be integrated with GCash, Maya, or other online payment services for secure transactions.

3. Data Flow Summary
Customers access Petalynx to browse flower products, place orders, and make payments. Shop owners upload and manage flower listings and process customer orders. All transaction, user, and product information is stored in Firebase Firestore. Administrators monitor system activities, manage users and shops, and generate reports. Data continuously flows between users, system processes, and databases to ensure accurate order processing and inventory management.

# Integration Pattern Overview

Hub and Spoke

Rationale
The hub-and-spoke integration is a good fit for Petalynx because customers, sellers, and admins need to work with shared information, especially user accounts, flower listings, and orders. Firebase provides a central place for authentication and data, so each part of the app can access the information it needs without building and maintaining a separate backend API. Firestore’s real-time listener also suits workflows such as keeping seller order views up to date.

This keeps the integration relatively simple for the project while supporting its core e-commerce workflows. The tradeoff is that Firebase becomes a central dependency, so access should be protected with carefully configured Firestore security rules and role-based permissions.