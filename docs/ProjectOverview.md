# petalynx
⌢瀠瑥污獳•਍# ITE412_SIA2_Lynxs_Petalynx

Hello, We are the Team Lynxs of BSIT IV F3

Our Title is "Petalynx"

Team Members:
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


# Integration Pattern Overview

Hub and Spoke

Rationale
The hub-and-spoke integration is a good fit for Petalynx because customers, sellers, and admins need to work with shared information, especially user accounts, flower listings, and orders. Firebase provides a central place for authentication and data, so each part of the app can access the information it needs without building and maintaining a separate backend API. Firestore’s real-time listener also suits workflows such as keeping seller order views up to date.

This keeps the integration relatively simple for the project while supporting its core e-commerce workflows. The tradeoff is that Firebase becomes a central dependency, so access should be protected with carefully configured Firestore security rules and role-based permissions.