# Advancing Manufacturing Through Artificial Intelligence

A full-stack Django web application that demonstrates the application of
Artificial Intelligence in modern manufacturing industries. The platform
integrates real Machine Learning models, Gemini AI (gemini-1.5-flash), and
data-driven dashboards to address key manufacturing challenges.

---

## Project Overview

This platform provides manufacturing companies, researchers, and industry
analysts with AI-powered tools for:

- Predicting machine failures before they occur
- Detecting product defects using computer vision
- Optimizing production processes with AI recommendations
- Assessing supply chain risks automatically
- Generating intelligent reports and strategic recommendations via Gemini AI

---

## Features

### AI Applications
- **Predictive Maintenance** — Random Forest model predicts machine failure
  from sensor data (temperature, vibration, pressure, runtime hours)
- **Quality Control** — Manual defect reporting with optional ResNet18
  image-based AI severity detection
- **Process Optimization** — Rule-based AI engine auto-generates
  context-aware recommendations based on process name and efficiency data
- **Supply Chain Risk** — Gradient Boosting model auto-predicts supplier
  risk level from 5 input features

### Gemini AI Integration (gemini-1.5-flash)
- **Recommendations** — Full AI-generated adoption recommendations for
  manufacturing topics
- **Challenge Analysis** — Deep 7-point analysis of manufacturing challenges
- **Report Summaries** — Auto executive summary on every admin report
- **Dashboard Insights** — Live AI-generated insights based on platform stats

### User Management
- Custom session-based authentication (no Django auth)
- Role-based access: Admin, Industry User, Researcher, Analyst
- Admin panel for managing users, content, reports, and system monitoring
- Profile management with password change

### Dashboard & Analytics
- Real-time stats for all modules
- Role-specific navigation (admin vs user)
- Responsive design with mobile sidebar

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python 3.11, Django 4.x |
| Database | MySQL (via mysqlclient) |
| ML Models | scikit-learn, joblib, numpy |
| AI Vision | PyTorch, torchvision, Pillow |
| Gemini AI | google-genai (gemini-1.5-flash) |
| Frontend | Bootstrap 5.3, Bootstrap Icons, Chart.js |
| Fonts | Google Fonts — Inter |
| Environment | python-decouple (.env) |

---

## Installation & Setup
### Create and Activate Virtual Environment
python -m venv AI_venv

# Windows
AI_venv\Scripts\activate

# Linux / Mac
source AI_venv/bin/activate

### Install Dependencies
pip install -r requirements.txt

### Create MySQL Database
CREATE DATABASE ai_manufacturing_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

### Run Migrations
python manage.py makemigrations
python manage.py migrate

### Train AI Models

1. Train Predictive Maintenance model (Random Forest)
python ai_models/train_model.py

2. Train Supply Chain Risk model (Gradient Boosting)
python ai_models/train_supply_model.py

### Seed Sample Data
python seed_data.py

### Start the Server
python manage.py runserver

