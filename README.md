# Wealthwise-asset-management-system
Asset Management System for Asset Management Companies

Overview

WealthWise is a desktop-based asset management system designed to help Asset Management Companies (AMCs) streamline asset tracking, client investment management, and comprehensive fund profiles. Built with Python and MySQL, it provides role-based access for AMC administrators, fund managers, and clients, complete with automated database triggers and PDF-based certification extraction.

Features

Authentication & Authorization:

AMC Admin login/register

Fund Manager login

Customer login

Asset Management: Add, view, and manage assets including shares and valuation.

Bank & Account Management: Manage bank details, account balances, and transactions.

Fund Management: Create and manage funds, view fund metrics (size, returns, balance).

Investment & Transactions:

Place buy/sell orders

Track transactions with automatic logging

Update fund balances via database triggers

Certification Extraction: Upload certificate PDFs and automatically extract certificate details using triggers and Python's PyPDF2.

Reporting: View top investors, fund performance, and custom queries.

Database Automation:

MySQL triggers for fund balance updates and transaction logs

Stored procedures for certificate management

Tech Stack

Language: Python 3.x

GUI: HTML,CSS,JavaScript, ReactJS

Database: MySQL

PDF Parsing: PyPDF2

Connector: mysql-connector-python

Project Structure

WealthWise-DBMS-for-AMCs-main/
├── DBMS Project Final Report - 196_200_194.pdf  # Detailed project report
├── queries.sql                                # SQL script to create database, tables, triggers, and procedures
├── dbms_proj.py                               # Main Python application
├── images/                                    # Icons and screenshots
│   ├── icon.ico
│   ├── wealth1.png
│   ├── wealth2.png
│   ├── wealth3.png
│   └── wealth4.png
└── README.md                                  # Project documentation

Setup & Installation

Clone the repository
git clone https://github.com/<your-username>/WealthWise-DBMS-for-AMCs.git
cd WealthWise-DBMS-for-AMCs-main

Database Setup

Ensure MySQL server is running.

Execute the SQL script to create the database, tables, triggers, and procedures:

mysql -u root -p < queries.sql

By default, the script creates a database named dbms.

Python Dependencies

Install required Python packages:

pip install mysql-connector-python PyPDF2

Configure Database Credentials

Edit dbms_proj.py and update the MySQL connection parameters at the top of the file:

db = mysql.connector.connect(
    host="localhost",
    user="root",
    password="your_password",
    database="dbms"
)

Run the Application

python dbms_proj.py

Usage

Launch the application.

Register or log in as an AMC admin.

Navigate to role-specific dashboards:

Fund Manager: create/manage funds and assets.

Customer: place investments and view portfolio.

Use the Certification Extraction feature to upload PDF certificates.

View reports and perform queries via GUI.
