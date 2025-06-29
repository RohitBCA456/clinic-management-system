# 🏥 Clinic Management System

A full-stack web application for managing patient registrations, prescriptions, and billing in a clinical environment. Includes role-based dashboards for receptionist and doctor, and enables generating & printing of medical documents.

---

## 🚀 Features

- 📝 **Receptionist Dashboard**
  - Register new patients
  - Generate and view tokens
  - View all patients
  - Generate bills for patients with prescriptions

- 👨‍⚕️ **Doctor Dashboard**
  - View patients by token
  - Add medical prescriptions
  - Access full patient history

- 📄 **Patient History & Billing**
  - View prescription and bill together
  - Separate views for printing & downloading

- 🔐 **Authentication**
  - Session-based login using cookies

---

## 🛠️ Tech Stack

### Backend
- Node.js
- Express.js
- MongoDB
- Mongoose

### Frontend
- HTML
- CSS
- JavaScript (Vanilla)
- Bootstrap (for styling)

---

## 📁 Project Structure

```
clinic-management-system/
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── database/
│   ├── app.js
│   ├── server.js
│   ├── .env
│   ├── package.json
│   └── package-lock.json
│
├── frontend/
│   ├── index.html                   # registration page                   
│   ├── login.html                   # Login page
│   ├── doctorDashBoard.html         # Doctor dashboard
│   ├── receptionistDashBoard.html   # Receptionist dashboard
│   ├── index.js
│   ├── login.js
│   ├── receptionistDashBoard.js
│   ├── doctorDashBoard.js
│   ├── index.css
│   ├── login.css
│   ├── doctorDashBoard.css
│   └── receptionistDashBoard.css
```

---

## ⚙️ Setup Instructions

### 📦 Prerequisites

- Node.js
- MongoDB

### 🔧 Environment Setup

Create `.env` file in `/backend`

```
PORT=5000
MONGODB_URI=mongodb://localhost:27017/clinicDB
JWT_SECRET=1234
ORIGIN= [your frontend url]
```

### 📥 Install Dependencies

```
cd backend
npm install
```

### ▶️ Run the Server

```
npm start
```

> Open `frontend/*.html` in the browser manually or use Live Server

---

## 🔐 Authentication

| Method | Route             | Description              |
|--------|-------------------|--------------------------|
| POST   | /auth/login       | Login as doctor/receptionist |
| GET    | /auth/getCurrentUser | Get current logged-in user |

---

## 👨‍⚕️ Doctor Module

| Method | Route                                   | Description                  |
|--------|------------------------------------------|------------------------------|
| GET    | /prescription/patients/token/:tokenId    | Fetch patient by token       |
| POST   | /prescription/create                     | Add prescription             |
| GET    | /prescription/history/:patientId         | View patient prescription history |

---

## 👩‍💼 Receptionist Module

| Method | Route                     | Description                   |
|--------|----------------------------|-------------------------------|
| POST   | /token/generate            | Register patient and generate token |
| GET    | /token/all                 | View all generated tokens     |
| POST   | /bill/create               | Generate a bill for a patient |
| GET    | /bill/:patientId           | Get bill for a specific patient |

---

## 🧾 Prescription & Billing UI

- 💊 Patient history shows both prescription and bill  
- 🖨️ Dedicated print/download views:
  - `printPrescription.html`
  - `printBill.html`

---

## 📦 Dependencies

- express  
- mongoose  
- dotenv  
- cookie-parser  
- cors  
- nodemon

---

## 🤝 Contributing

```
git clone https://github.com/RohitBCA456/clinic-management-system.git
cd clinic-management-system/backend
npm install
npm start
```

---

## 📄 License

MIT License © [Rohit Yadav](https://github.com/RohitBCA456)
