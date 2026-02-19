# Full-Stack App (Student Build)

A static frontend prototype that simulates a full-stack web application — including authentication, role-based access control, and CRUD operations — entirely in the browser using `localStorage`. Built as a learning exercise before backend integration.

---

## 🚀 Features

- **User Registration** with simulated email verification
- **Login / Logout** with session management
- **Role-Based Access Control** — Admin and User roles with different navigation and permissions
- **Profile Management** — View and edit your own profile
- **Requests** — Users can submit and view equipment, leave, or resource requests
- **Employees** — Admins can create, edit, and delete employee records
- **Departments** — Admins can manage department listings
- **Accounts** — Admins can manage all user accounts, including password resets
- **Toast Notifications** — Real-time feedback for all actions
- **Dark / Midnight UI Theme** with pill-style buttons

---

## 📁 File Structure

```
├── index.html       # Main HTML file — all pages and modals
├── style.css        # Styling — dark theme, layout, components
└── script.json      # JavaScript logic (rename to script.js)
```

> ⚠️ **Note:** `script.json` should be renamed to `script.js`. It contains JavaScript, not JSON. Update the `<script>` tag in `index.html` accordingly.

---

## 🔧 Setup

No build tools or dependencies required. Just open `index.html` in any modern browser.

```bash
# Clone or download the project
# Then simply open index.html in your browser
open index.html
```

---

## 🔐 Default Admin Account

On first load, a default admin account is automatically created:

| Field    | Value               |
|----------|---------------------|
| Email    | admin@example.com   |
| Password | admin123            |
| Role     | Admin               |

---

## 🗃️ Data Storage

All data is stored in the browser's `localStorage` under the key `ipt_demo_v1`. The data structure includes:

```json
{
  "accounts": [],
  "departments": [],
  "employees": [],
  "requests": []
}
```

> ⚠️ Clearing your browser's localStorage or opening in a private/incognito window will reset all data to defaults.

---

## 📦 Default Departments

The following departments are seeded on first load:

- Engineering
- HR (Human Resources)
- Finance
- IT (Information Technology)
- Accounting
- Marketing

---

## 🧭 Pages Overview

| Page        | Access       | Description                              |
|-------------|--------------|------------------------------------------|
| Home        | Public       | Landing page with app overview           |
| Register    | Public       | Create a new user account                |
| Verify      | Public       | Simulate email verification step         |
| Login       | Public       | Authenticate with email and password     |
| Profile     | Logged In    | View and edit your profile               |
| Requests    | Logged In    | Submit and view personal requests        |
| Employees   | Admin Only   | Manage employee records                  |
| Departments | Admin Only   | Manage department listings               |
| Accounts    | Admin Only   | Manage all user accounts                 |

---

## 🛠️ Tech Stack

- **HTML5** — Structure and pages
- **CSS3** — Custom dark theme styling
- **Vanilla JavaScript** — All logic, routing, and state management
- **Bootstrap 5** — Additional UI utilities via CDN
- **localStorage** — Client-side data persistence

---

## ⚠️ Known Issues / Limitations

- `script.json` must be renamed to `script.js` to work correctly
- Passwords are stored in plain text in `localStorage` — not suitable for production
- No real backend or database; all data resets if localStorage is cleared
- No real email verification; it is simulated client-side

---

## 📌 Planned Improvements

- Connect to a real REST API backend (e.g. Node.js + Express)
- Implement JWT-based authentication
- Add a real database (e.g. MySQL, PostgreSQL, MongoDB)
- Hash passwords before storing
- Add form validation with error messages

---

## 👨‍💻 Author

Built as a student project for learning full-stack web development concepts.
