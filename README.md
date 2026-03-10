# CMS Flask Web App

A simple Content Management System (CMS) built with **Flask**, deployed on **Azure App Service**.  
Supports both local admin login and **Microsoft Entra (Azure AD) login**, with image uploads stored in Azure Blob Storage. Login attempts are logged for monitoring.

---

## Features

- Admin login (username/password)
- Microsoft Entra login (OAuth)
- Create, edit posts with images
- Azure Blob Storage integration for storing post images
- Logging of access attempts:
  - Successful login
  - Failed login
- Deployed on Azure App Service

---

## Requirements

- Python 3.11
- Flask
- Flask-Login
- Flask-SQLAlchemy
- MSAL (Microsoft Authentication Library)
- pyodbc (for SQL Server)
- Azure subscription with:
  - App Service
  - SQL Database
  - Blob Storage

---

## Setup Instructions

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/cms-flask-app.git
cd cms-flask-app
```
2. **install requirements**
```bash
pip install -r requirements.txt
```
3. **Configure environment variables**
Set the following in your local environment or in Azure App Service → Configuration → Application settings:
```bash
SECRET_KEY=<your_secret>
BLOB_ACCOUNT=<your_storage_account_name>
BLOB_CONTAINER=images
BLOB_STORAGE_KEY=<your_blob_storage_key>
SQL_SERVER=<your_sql_server>.database.windows.net
SQL_DATABASE=cms
SQL_USER_NAME=<your_sql_username>
SQL_PASSWORD=<your_sql_password>
CLIENT_ID=<your_azure_app_client_id>
CLIENT_SECRET=<your_azure_app_client_secret>
```

4. **Run the app locally**

```bash
flask run
```
5. **Access the app locally**
```bash
http://127.0.0.1:5000
```
6. **Deploy to Azure**

7. **Push your code to GitHub.**

In Azure App Service → Deployment Center, connect to GitHub repository.

Ensure the same environment variables are set in App Service → Configuration → Application settings.

## Screenshots / Evidence

- Article created with image
- SQL tables and query results
- Blob Storage endpoint
- Redirect URI configuration in Azure
- Python app running with header "Article CMS"
- Create new post option
- After logout scenario
- Login scenario
- Successful and failed login attempts logged: log-solution.png
