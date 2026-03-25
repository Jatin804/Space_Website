# 🌌 Space Explorer — Django Project

A Django-based web application that provides information about the **Solar System**, **Universe**, and includes an interactive **FAQs** section along with a **Reviews system powered by MySQL**.

---

## 🚀 Features

* 🌍 Informational pages about the Universe & Solar System
* ❓ FAQs section
* 📝 Contact form (stored in database)
* ⭐ Reviews system using MySQL
* 🛠 Django backend with database integration

---

## 🧱 Tech Stack

* **Backend:** Django
* **Database:** SQLite → MySQL Migration
* **Frontend:** HTML, CSS
* **DB Client:** MySQL Client

---

## ⚙️ Setup & Installation Guide

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/space-explorer.git
cd space-explorer
```

---

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

---

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔄 Database Migration: SQLite → MySQL

### 4️⃣ Install MySQL Client

```bash
pip install mysqlclient
```

> ⚠️ Make sure you are using **Python 3.12**, as compatibility matters for MySQL client installation.

---

### 5️⃣ Create MySQL Database

Run the following in your MySQL shell:

```sql
CREATE DATABASE reviews
CHARACTER SET utf8mb4 
COLLATE utf8mb4_general_ci;
```

---

### 6️⃣ Configure Django Database Settings

Update your `settings.py`:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'reviews',        # Database name
        'USER': 'root',           # MySQL username
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```

---

### 7️⃣ Apply Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

---

### 8️⃣ Run Development Server

```bash
python manage.py runserver
```

Visit: `http://127.0.0.1:8000/`

---

## 🧩 Database Model

```python
from django.db import models

class Contact(models.Model):
    name = models.CharField(max_length=122)
    email = models.CharField(max_length=122)
    phone = models.CharField(max_length=15)
    desc = models.TextField()
    date = models.DateField()

    def __str__(self):
        return self.name
```

---

## 📸 Project Screenshots

### 🌌 Home / Main Page

![Screenshot 2024-04-07 112143](https://github.com/Jatin804/Projects/assets/146949850/c46ad911-f573-416d-a7b2-520e32ea0dbf)

---

### 🌠 The Universe Page

![Screenshot 2024-04-07 112315](https://github.com/Jatin804/Projects/assets/146949850/56f44a7b-59a0-49c3-a0f4-be7ce239682a)

---

### 🪐 Solar System Page 1

![Screenshot 2024-04-07 112414](https://github.com/Jatin804/Projects/assets/146949850/641ef0c9-deec-4b81-986d-48cd88185731)

---

### 🪐 Solar System Page 2

![Screenshot 2024-04-07 112659](https://github.com/Jatin804/Projects/assets/146949850/b9ccfbf0-3def-450f-aebe-50ab76f33123)

---

### ❓ FAQs Page

![Screenshot 2024-04-07 112914](https://github.com/Jatin804/Projects/assets/146949850/a0f814c4-e7d0-408e-bafd-04bf990541bc)

---

### ⭐ Reviews Page

![Screenshot 2024-04-07 113136](https://github.com/Jatin804/Projects/assets/146949850/f481aae0-1bf7-4178-9557-483207295943)

---

### 🗄 Django Backend Database

![Screenshot 2024-04-07 111856](https://github.com/Jatin804/Projects/assets/146949850/a801165f-56cf-405b-9b48-10d6a4405b9e)

---

## 📌 Important Notes

* Ensure **MySQL server is running** before starting Django
* Double-check database credentials
* Python **3.12 compatibility is required**
* Always run migrations after DB changes

---

## 🤝 Contribution

Feel free to fork the repository and submit pull requests!

---

## 📄 License

This project is for educational purposes.

---
