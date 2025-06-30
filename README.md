# 📖 Django Learning Progress Tracker

---

## 📆 DAY 1: Django Setup

### ✅ Creating a Virtual Environment

```bash
python -m venv {venv-name}
```

> **Recommended Setting:** Set ExecutionPolicy to RemoteSigned. This allows us to run local scripts without any restrictions. Downloaded scripts can run if signed by a trusted publisher.

### ✅ Activating the Virtual Environment

```bash
.\{venv-name}\Scripts\activate
```

### ✅ Installing Django

```bash
pip install django
```

> **Recommended Practice:** Save the list of packages and their versions into a file called <code>requirements.txt</code>. This enables us to recreate the exact environment when sharing or deploying. Command: <code>**pip freeze > requirements.txt**</code>
