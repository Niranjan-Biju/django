# 📖 Django Learning Progress Tracker

---

## 📆 DAY 1: Django Setup

### ✅ Creating a Virtual Environment

```bash
python -m venv {venv-name}
```

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
* Multiple apps can exist within the same project
* Change working directory to project folder

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
> Add <app-name> to **INSTALLED_APPS** in <code>settings.py</code>
