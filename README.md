# ◈ Spendly — Personal Expense Tracker

A **Python Flask** web application for tracking personal expenses. Users can log expenses, categorize their spending, and understand where their money goes — one transaction at a time.

> 🚧 **This project is under active development.** Core UI and routing are complete; database logic and full CRUD features are being implemented step by step.

---

## ✨ Features

### ✅ Implemented
- 🏠 Landing page with expense category breakdown preview
- 📋 User registration form (name, email, password)
- 🔐 User login form
- 🧭 Navbar with Sign in / Get started links
- 🎨 Clean UI with DM Sans + DM Serif Display fonts

### 🔜 Planned / In Progress
- 🗄️ SQLite database setup (`get_db`, `init_db`, `seed_db`)
- 🔒 Session-based authentication (register, login, logout)
- 👤 User profile page
- ➕ Add expense
- ✏️ Edit expense
- 🗑️ Delete expense
- 📊 Spending summary by category and date range

---

## 🏗️ Tech Stack

| Technology | Purpose |
|---|---|
| **Python 3** | Backend language |
| **Flask 3.1** | Web framework |
| **SQLite** | Lightweight relational database |
| **Jinja2** | HTML templating (via Flask) |
| **Werkzeug** | Password hashing & utilities |
| **CSS3** | Custom styling |
| **JavaScript** | Frontend interactivity |

---

## 📁 Project Structure

```
spendly/
│
├── app.py                  # Flask app & all route definitions
│
├── database/
│   ├── __init__.py
│   └── db.py               # get_db(), init_db(), seed_db() — to be implemented
│
├── templates/
│   ├── base.html           # Base layout (navbar + footer)
│   ├── landing.html        # Home / marketing page
│   ├── register.html       # User registration form
│   └── login.html          # User login form
│
├── static/
│   ├── css/
│   │   └── style.css       # All custom styles
│   └── js/
│       └── main.js         # Frontend JS
│
└── requirements.txt        # Python dependencies
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or higher
- pip

### 1. Clone the Repository

```bash
git clone https://github.com/LOKESH-sys365/spendly.git
cd spendly
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate        # macOS / Linux
venv\Scripts\activate           # Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the App

```bash
python app.py
```

Open [http://localhost:5001](http://localhost:5001) in your browser.

---

## 🛣️ Routes Overview

| Method | Route | Status | Description |
|---|---|---|---|
| GET | `/` | ✅ Done | Landing page |
| GET | `/register` | ✅ Done | Registration form |
| GET/POST | `/login` | ✅ Done | Login form |
| GET | `/logout` | 🔜 Step 3 | Logout & clear session |
| GET | `/profile` | 🔜 Step 4 | User profile page |
| GET/POST | `/expenses/add` | 🔜 Step 7 | Add new expense |
| GET/POST | `/expenses/<id>/edit` | 🔜 Step 8 | Edit an expense |
| GET/POST | `/expenses/<id>/delete` | 🔜 Step 9 | Delete an expense |

---

## 🗄️ Database (Coming in Step 1)

The `database/db.py` file will contain:

```python
def get_db():
    # Returns a SQLite connection with row_factory and foreign keys enabled

def init_db():
    # Creates all tables using CREATE TABLE IF NOT EXISTS

def seed_db():
    # Inserts sample data for development
```

Planned tables:
- `users` — id, name, email, password_hash
- `expenses` — id, user_id, category, amount, description, date

---

## 🧪 Testing

This project uses **pytest** and **pytest-flask** for testing.

```bash
pytest
```

---

## 📦 Dependencies

```
flask==3.1.3
werkzeug==3.1.6
pytest==8.3.5
pytest-flask==1.3.0
```

---

## 🗺️ Development Roadmap

- [x] Step 0 — Project setup & static UI
- [ ] Step 1 — Database setup (SQLite)
- [ ] Step 2 — User registration with password hashing
- [ ] Step 3 — Login / Logout with sessions
- [ ] Step 4 — User profile page
- [ ] Step 5 — List all expenses
- [ ] Step 6 — Filter expenses by date/category
- [ ] Step 7 — Add expense
- [ ] Step 8 — Edit expense
- [ ] Step 9 — Delete expense

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

> ◈ **Spendly** — Track every rupee. Own your finances.
