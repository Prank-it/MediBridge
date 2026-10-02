# 🏥 MediBridge

### AI-Powered Healthcare Access for Rural & Underserved Communities

MediBridge is a healthcare accessibility platform designed to bridge the gap between patients in rural and underserved areas and qualified healthcare professionals.

The platform combines **teleconsultation, appointment management, digital medical records, AI-assisted healthcare features, and AI voice calling** to make healthcare access more convenient, especially for patients facing distance, specialist availability, language, and connectivity challenges.

---

## 🎯 Problem

People in rural and underserved areas often face challenges such as:

* Long travel distances to reach specialists
* Limited availability of doctors
* Delayed referrals and consultations
* Fragmented medical records
* Difficulty understanding medical information
* Language and health-literacy barriers
* Limited access to diagnostics and medicines
* Poor connectivity and limited digital access

MediBridge aims to provide a single platform that connects patients, doctors, and healthcare services.

---

## 💡 Solution

MediBridge provides a digital healthcare ecosystem where patients can:

* Find doctors based on specialization
* Book appointments
* Attend remote consultations
* Maintain digital medical records
* Upload medical documents
* Access prescriptions
* Receive AI-assisted medical information
* Get assistance through regional-language AI
* Use an AI calling assistant for appointment-related tasks

Doctors can manage appointments, access relevant patient information, conduct consultations, and provide digital prescriptions.

---

## 🚀 Key Features

### 👤 Patient

* Patient registration and login
* JWT-based authentication
* Patient profile
* Doctor discovery
* Specialization-based doctor recommendations
* Appointment booking
* Appointment history
* Remote and offline appointment options
* Medical document upload
* Digital prescriptions
* AI-assisted healthcare information
* Multilingual assistance

### 👨‍⚕️ Doctor

* Doctor registration and login
* Doctor profile
* Specialization
* Experience and location
* Available appointment slots
* Appointment management
* Patient information access
* Digital prescription generation
* Remote consultation through Google Meet

### 🤖 AI Features

* AI-assisted specialty recommendation
* Prescription/medicine information extraction
* Medical document OCR
* AI-generated medicine explanations
* English and Hindi assistance
* Text-to-speech support
* AI voice calling assistant

### 📞 AI Calling Agent

MediBridge includes an AI-powered voice assistant designed to help users with appointment-related tasks.

The assistant can support:

* Doctor/category selection
* Appointment booking
* Appointment rescheduling
* Appointment cancellation
* Appointment status checking
* Bilingual interaction

The goal is to make healthcare services accessible even to users who may have difficulty navigating a conventional web interface.

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │       Patient       │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   React Frontend    │
                    │      + Vite         │
                    └──────────┬──────────┘
                               │
                         REST APIs
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Flask Backend    │
                    ├─────────────────────┤
                    │ Authentication      │
                    │ Patient APIs         │
                    │ Doctor APIs          │
                    │ Appointment APIs     │
                    │ Prescription APIs    │
                    │ Medical Documents   │
                    └──────────┬──────────┘
                               │
                     ┌─────────┴─────────┐
                     ▼                   ▼
              ┌─────────────┐    ┌─────────────┐
              │   SQLite    │    │ AI Services │
              │  Database   │    │ OCR / LLM   │
              └─────────────┘    └─────────────┘
                                      │
                                      ▼
                              AI Calling Agent
```

---

## 🛠️ Tech Stack

### Frontend

* React
* Vite
* Tailwind CSS
* JavaScript

### Backend

* Python
* Flask
* REST APIs
* JWT Authentication
* SQLite

### AI & APIs

* Google Gemini
* NVIDIA Nemotron OCR
* Google Meet
* AI Voice/Calling APIs

### Development Tools

* Git
* GitHub
* VS Code

---

## 🔐 Authentication

MediBridge uses JWT-based authentication with role-based access for:

* Patients
* Doctors

Protected APIs ensure that users can access functionality according to their role.

---

## 🗄️ Database

The project uses **SQLite** for persistent data storage.

The database manages information such as:

* Users
* Patients
* Doctors
* Medical documents
* Appointments
* Prescriptions

The project was migrated from a local JSON-based data approach to SQLite for more structured and persistent data management.

---

## 👨‍💻 My Contribution

MediBridge was developed as a **team project for the Smart India Hackathon (SIH)**.

My primary responsibility was **backend development and integration**.

### Backend Contributions

* Designed and implemented REST APIs using Flask
* Implemented patient-related APIs
* Implemented doctor-related APIs
* Implemented JWT authentication and role-based access
* Developed appointment management APIs
* Implemented medical document handling
* Implemented prescription-related functionality
* Integrated backend APIs with the React frontend
* Worked on SQLite database migration
* Integrated external AI/API services
* Worked on the AI calling workflow and appointment-related backend logic
* Handled backend configuration and environment-based API credentials

---

## 📂 Project Structure

```text
MediBridge-AICalling-Dev/
│
├── MediBridge/
│   ├── backend/
│   ├── frontend/
│   └── ...
│
├── .gitignore
└── README.md
```

---

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Prank-it/MediBridge.git
cd MediBridge
```

### 2. Backend Setup

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

### 3. Environment Variables

Create a `.env` file and configure the required API keys.

Example:

```env
SECRET_KEY=your_secret_key
GOOGLE_API_KEY=your_google_api_key
NVIDIA_API_KEY=your_nvidia_api_key
```

Do **not** commit API keys or secrets to GitHub.

### 4. Run the Backend

```bash
python app.py
```

The backend runs locally on:

```text
http://127.0.0.1:5000
```

### 5. Run the Frontend

```bash
npm install
npm run dev
```

---

## 🔒 Security

API keys and other sensitive credentials are stored using environment variables and should never be committed to the repository.

The `.env` file should be included in `.gitignore`.

---

## 📸 Screenshots

Screenshots of the MediBridge interface can be added here.

```text
Coming soon
```

---

## 🔮 Future Improvements

* Better low-connectivity support
* Regional-language voice interaction
* Basic-phone accessibility through voice calls
* Improved AI-based triage
* Healthcare facility dashboards
* Medicine availability integration
* Diagnostic center integration
* Interoperable medical records
* Emergency escalation workflows
* Deployment with production-grade infrastructure

---

## 👥 Team Project

MediBridge was developed collaboratively as part of the **Smart India Hackathon (SIH)**.


The project involved contributions across:

* Backend development
* Frontend development
* AI integration
* UI/UX
* Voice/Calling systems
* Database and API integration

## Members
https://github.com/ShreshthMishra0212
https://github.com/Mehardeep-Singh-Arneja
https://github.com/harshilguptahgs2007-ux

---

## 📌 Project Status

**Prototype / Hackathon Project**

MediBridge is an ongoing project and may continue to evolve with additional features, integrations, and production improvements.

---

## 📄 License

This project is intended for educational, hackathon, and demonstration purposes.
