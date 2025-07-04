# 📖 Django Learning Progress Tracker

---

## 📆 DAY 1: Django Setup

### ✅ Creating a Virtual Environment

```bash
python -m venv {venv-name}
```
* Create a venv for each project to avoid version conflicts or dependency problems.
  
> **Recommended Setting:** Set powershell ExecutionPolicy to RemoteSigned. This allows us to run local scripts without any restrictions. Downloaded scripts can run if signed by a trusted publisher.

### ✅ Activating the Virtual Environment

```bash
.\{venv-name}\Scripts\activate
```

### ✅ Installing Django

```bash
pip install django
```

> **Recommended Practice:** Save the list of packages and their versions into a file called <code>requirements.txt</code>. This enables us to recreate the exact environment when sharing or deploying. Command: <code>**pip freeze > requirements.txt**</code>

##   DAY 2: Creating a Django Project and App

### ➡️ Creating the Django project

```bash
django-admin startproject <project-name>
```
* Multiple apps can exist within the same project.
* Change working directory to project folder.

### ➡️ Creating the app

```bash
python manage.py startapp <app-name>
```
> In Django, the "project" is the overall container, and "apps" are components (e.g., blog, users, products, etc.)

### ➡️ Running the project

```bash
python manage.py runserver
```

### ➡️ Register the app in settings
> Add <app-name> to **INSTALLED_APPS** in <code>settings.py</code>.

## ⏭️Next step: Connecting the view to user-accessible URL(Basic)

> <code>views.py</code> -> Define a function to accept a HTTP request and return an appropriate HTTP response.

> <code>{app-name}/urls.py</code> -> It is used to map the URL to views.

> <code>{project-name}/urls.py</code> -> Maps incoming requests to the appropriate app’s URL configuration.

---

## DAY 3: Important Django Files

### <code>**manage.py**</code>

* Enables us to interact with the Django project via terminal.

### <code>**settings.py**</code>

* It contains all project-wide settings.
* It is the main configuration file for:

  * Installed apps

  * Database setup

  * Static files

  * Middleware

  * Templates

  * Security keys
 
### <code>**urls.py(Project)**</code>

* To route the HTTP requests to the specified app.

### <code>**urls.py(App)**</code>

* To map URL to the necessary view.
* Not automatically created by Django.

### <code>**views.py**</code>

* Contains functions that accepts HTTP requests and return appropriate HTTP response.

### <code>**models.py**</code>

* Defining database structure.

## 🔄 Django Request-Response Cycle

<code>HTTP Request</code> → <code>Web Server</code> → <code>WSGI/ASGI</code> → <code>Middleware (Authentication, Log Requests, etc.)</code> → <code>URL Routing</code> → <code>View Function Returns a Response</code> → <code>Middleware (Add Cookies, Log Response, etc.)</code> → <code>Sent Response to the Browser</code>

---
