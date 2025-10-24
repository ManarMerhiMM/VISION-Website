# VISION Website — React Frontend for the Wearable Ecosystem for the Visually Impaired

**VISION (Wearable Ecosystem for the Visually Impaired)** is an integrated assistive technology platform that enhances the **mobility, autonomy, and safety** of visually impaired individuals.  
This repository hosts the **React-based** website, serving as a user-friendly interface that allows users to monitor analytics and configure their accounts. It acts as a secure, centralized portal for caregivers, doctors, and authorized users to access statistics, alerts, and configuration tools.

---

## System Architecture

The VISION ecosystem consists of three main layers working together:

- **Frontend (React.js):** Web dashboard for user management, data visualization, and configuration (this repo).
- **Mobile App (React Native):** Interfaces with the wearable system, presents real-time biometrics, and syncs with this API.
- **Backend (Laravel API):** Central hub for authentication, data persistence, and business logic.
- **Database (MySQL):** Stores all persistent data, accessible only through the API.

---

## ⚙️ Features

- 📊 **Dashboard & data visualization** for historical readings, device statistics, and trends
- 🧩 **Forms & client-side validation** for settings, preferences, and updates
- 🗂️ **State management & caching** using Context or Redux for UI state
- ♿ **Responsive & accessible UI** for desktop and tablet screens, also accessibility tools dedicated to the visually-impaired are implemented
- 🗃️ **Exporting & reporting** of historical data as CSV or PDF (admin-only)

♿ Responsive & accessible UI for desktop and tablet

## 🧰 Tech Stack

| Layer           | Technology                          |
| --------------- | ----------------------------------- |
| Framework       | React 19.1.1                        |
| Authentication  | Laravel Sanctum (API Tokens)        |
| API Format      | REST (JSON)                         |
| Frontends       | React (Web) + React Native (Mobile) |
| Version Control | Git & GitHub                        |

---

# 🚀 Getting Started (Local Development)

Follow these steps to run the **VISION React frontend** locally:

### 1️⃣ Clone the repository

```bash
git clone https://github.com/ManarMerhiMM/VISION-Website.git
cd vision-frontend
```

### 2️⃣ Install dependencies

```bash
npm install
```

### 3️⃣ Configure environment variables

All can be found in the .env file

### 4️⃣ Start the development server

```bash
npm run dev
```

### 5️⃣ Build for production

```bash
npm run build
```

### 6️⃣ Preview production build

```bash
npm run preview
```

## 🔒 Security Practices

- ✅ Secure API communication — all requests are made over HTTPS to prevent interception or tampering.
- ✅ Token-based authentication — the website authenticates via Laravel Sanctum tokens, stored securely (not in localStorage).
- ✅ CORS-compliant configuration — requests are only made to the official VISION API origin.
- ✅ Environment-based configuration — sensitive values like API URLs and keys are stored in .env files (never hardcoded).
- ✅ Client-side input validation — all forms are validated before submission to reduce backend load and prevent bad data.
- ✅ Session and role management — user sessions respect access levels (Admin and standard user).
- ✅ Preventive UI design — components handle errors gracefully and sanitize displayed data.
- ✅ No exposure of sensitive data — debug logs and environment details are disabled in production builds.

## 🧠 System Data Flow (concerning the website and mobile application)

1. Raspberry Pi collects live processed biometric data (SPO2 and BPM).
2. React Native mobile app connects via BLE and displays the data (live).
3. Mobile app periodically sends readings to the Laravel API over HTTPS.
4. API validates, stores, and aggregates readings in MySQL.
5. React web dashboard retrieves data via the same API to display user statistics, device logs, and analytics.

## 👥 Contributors

**VISION Development Team**  
Final Year Project — Computer Engineering Department

| Role                            | Name                |
| ------------------------------- | ------------------- |
| Backend Developer               | Manar Merhi         |
| Frontend Developer (Web)        | Malek Shibli        |
| Mobile Developer (React Native) | Manar Merhi         |
| Embedded Systems / Hardware     | Mohammad Shaaban    |
| Computer Vision and ML          | Mohammad El Halabi  |
| Biometric Processing            | Abdulrahman Nakouzi |

### 📄 License

This project is developed for **academic** and **research** purposes.

###### © 2025 VISION Project Team — All rights reserved.
