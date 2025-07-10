# 🌱 MSME CarbonTrack

**MSME CarbonTrack** is a Flask-based web platform designed to help Micro, Small, and Medium Enterprises (MSMEs) in India **track, monitor, and reduce their carbon footprint**. The application enables businesses to log their carbon-emitting activities, visualize their emissions through interactive charts, and stay within their prescribed carbon limits based on government guidelines.

---

## 🚀 Features Implemented

### ✅ 1. User Authentication & Business Profile
- Secure registration and login system (with hashed passwords using `passlib`).
- Registration form includes:
  - Business Name
  - Owner Name
  - Email & Password
  - MSME Category (Micro / Small / Medium)
  - Business Type
- User information is stored in a structured SQLAlchemy model using MySQL.

---

### ✅ 2. Dashboard (User Overview)
- Shows summarized statistics:
  - **This Month's Emissions**
  - **This Year’s Emissions**
  - **All-Time Emissions**
- Includes a **progress bar component**:
  - Displays emissions used vs. limit.
  - Color-coded progress (Green, Orange, Red).
  - Emoji feedback for user-friendly interpretation.
  - **Switch between Monthly and Yearly views** with smooth, no-reload updates using `fetch()`.

---

### ✅ 3. Activities Page (Log Carbon Emissions)
- Users can **log activities** via a Bootstrap modal form.
  - Input fields: `category`, `sub_type`, `value`, `unit`, and `date`.
- Activities are stored in the `Emission` table.
- Displays:
  - **Recent Activities Table**
  - **All Logged Activities**
- Each activity shows:
  - Serial No, Date, Category, Sub-type, Value, Unit, and Emissions in kg CO₂.
- Includes actions for:
  - 📝 Edit (opens modal with prefilled values)
  - 🗑️ Delete (removes activity via backend route)

---

### ✅ 4. Summary Page (Visual Emission Insights)
- Pie Chart: Emissions distribution by category (using Chart.js).
- Bar Chart:
  - Interactive filtering: monthly/yearly views
  - Custom dropdown to select year & month
  - Uses `fetch()` to update charts dynamically without page reload.
- Line Chart: Trend of emissions over the months (area-style line graph).

---

### ✅ 5. Sidebar Navigation (Fixed & Collapsible)
- Collapsible Bootstrap sidebar with icons.
- Sticky (fixed) sidebar that remains in place during scroll.
- Hamburger icon toggles the sidebar (shows ❌ when expanded and ☰ when collapsed).
- Active state highlighting for each page.

---

## 🔧 Technologies Used

- **Backend**: Python, Flask, SQLAlchemy ORM
- **Frontend**: Bootstrap 5, HTML5, CSS, JavaScript
- **Database**: MySQL
- **Charts & Visuals**: Chart.js
- **Authentication**: Custom logic with `passlib` for hashing

---

## 🧪 Planned Features (Coming Soon)

### 🔄 1. In-Place Editing for Activities
- Allow users to update activities using AJAX, without reloading the page.

### 📤 2. PDF & Excel Reports
- Generate downloadable reports summarizing emissions by category and time range.

### 📈 3. Advanced Analytics
- More chart types: stacked bars, radar, comparative views.
- Forecasting emissions based on current activity patterns.

### 🛠️ 4. Sector-Wise Recommendations
- Offer sector-specific suggestions to reduce emissions.
- Show cleaner alternatives and potential carbon savings.

### 📬 5. Notification System
- Alerts for exceeding carbon thresholds.
- Email notifications and dashboard popups.

### 🛡️ 6. Admin Panel
- Manage users, review emission logs, approve reports.

---

## 🧰 Installation Guide

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/msme-carbontrack.git
cd msme-carbontrack
