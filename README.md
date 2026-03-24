<div align="center">

# 🤍 MaaSuraksha
### *Gentle Care for Every Mother*

[![Live Demo](https://img.shields.io/badge/🌐_Live_Demo-maasuraksha.vercel.app-pink?style=for-the-badge)](https://maasuraksha.vercel.app)
[![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-Backend-black?style=for-the-badge&logo=flask)](https://flask.palletsprojects.com)
[![Vercel](https://img.shields.io/badge/Deployed_on-Vercel-000000?style=for-the-badge&logo=vercel)](https://vercel.com)

> A calm, AI-assisted maternal health screening and daily care tracking system — built for mothers and ASHA workers.

</div>

---

## About

**MaaSuraksha** (मा सुरक्षा — *Mother's Safety*) is an AI-powered maternal health screening web application that helps pregnant women and ASHA (Accredited Social Health Activist) workers identify pregnancy-related risk levels early.

Developed as part of a **Capstone Research Project**, the system classifies maternal risk into **Low**, **Mid**, or **High** based on clinical inputs, and allows daily wellness tracking for expectant mothers.

---

## Features

- **AI Risk Screening** — Predicts maternal risk level using a trained ML model
- **Daily Wellness Tracker** — Log mood, water intake, sleep, and symptoms
- **ASHA Dashboard** — View recent screening alerts and patient records
- **Role-Based Auth** — Separate experience for Patients and ASHA Workers
- **Dark / Light Mode** — Comfortable in any environment
- **Multilingual Support** — Language toggle for regional accessibility
- **Responsive Design** — Mobile-friendly for field use

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| Backend | Python, Flask |
| Database | SQLite |
| ML Model | scikit-learn, joblib, NumPy |
| Deployment | Vercel |

---

## ML Model

The model (`maternal_risk_model.pkl`) is trained on the UCI Maternal Health Risk Dataset and uses: `Age`, `DiastolicBP`, `BloodSugar`, `BodyTemp`, and `HeartRate` as features.

**Output:** `Low Risk` · `Mid Risk` · `High Risk`

---

## Project Structure

```
maasuraksha/
├── app.py                    # Flask backend
├── maternal_risk_model.pkl   # Trained ML model
├── index.html
├── form.html
├── dashboard.html
├── tracker.html
├── login.html
├── css/
├── js/
└── assets/
```

---

## Local Setup

```bash
git clone https://github.com/your-username/maasuraksha.git
cd maasuraksha
pip install flask joblib numpy scikit-learn
python app.py
```

App runs at `http://localhost:5000`

**Demo credentials:**

| Role | Username | Password |
|------|----------|----------|
| Patient | `mother1` | `mother123` |
| ASHA Worker | `asha1` | `asha123` |

---

## API Reference

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/login` | Login |
| POST | `/api/auth/signup` | Register |
| POST | `/api/predict` | Get risk prediction |
| GET | `/api/alerts` | Fetch screening history |
| POST | `/api/tracker` | Save wellness log |
| GET | `/api/tracker` | Get recent logs |

---

## Research Context

This project is part of a **Capstone Research Project** exploring AI-assisted maternal health screening for community health workers in rural India. The focus is on early risk identification with minimal clinical data and low-literacy-friendly interface design.

---

> ⚠️ **Disclaimer:** MaaSuraksha is a screening support tool only and is not a substitute for professional medical diagnosis.
