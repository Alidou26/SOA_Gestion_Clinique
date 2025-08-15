<div align="left"> <a href="./README.md">🇫🇷 Français</a> | <a href="./README.en.md">🇬🇧 English</a> </div>

---

<a name="top"></a>

<div align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/SpringBoot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot">
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis">
  <h1>SOA Telemedicine Clinic Management Application</h1> 
  <p>Project developed for the Service Oriented Architecture (SOA) module — Management of appointments, medical records, prescriptions, doctors, notifications, and patient follow-up.</p>
</div>

# [Demo Video](https://drive.google.com/file/d/16vmIgzZ3hDcO7jv7JHTnSts2dxmiRWFw/view?usp=sharing)
If the link doesn't work, please copy and paste it into your browser's address bar.

# [Report](https://drive.google.com/file/d/1l2pLChcDsLKM7mcFlVI1TMBrnPrlBmQI/view?usp=sharing)
If the link doesn't work, please copy and paste it into your browser's address bar.

## Table of Contents
1. [Introduction](#introduction)
2. [Key Features](#features)
3. [Technologies Used](#tech)
4. [Architecture](#architecture)
5. [Installation](#installation)
6. [Tests and Demonstrations](#demo)
7. [Future Improvements](#future)
8. [Application Demo](#app)

---

## Introduction<a name="introduction"></a>
This project aims to design a comprehensive information system for **managing a telemedicine clinic**, based on a **service-oriented architecture (SOA)**.  
It integrates **3 SOAP services** (medical records management, prescriptions, doctors) and **3 REST services** (appointment management, notifications, patient follow-up), orchestrated via a **BPMN process**.

The system enables:
- Complete management of patient data, doctors, prescriptions, and appointments
- Automated notification (email) sending
- Visualization of consultation history and reports
- Seamless orchestration between services via Redis

<div align="right">
  <a href="#top">⬆ Back to top</a>
</div>

---

## Key Features<a name="features"></a>

### 🧑‍⚕ SOAP Management
- **Patients**: Add, modify, delete, view
- **Doctors**: Add, modify, delete, view
- **Medical records**: Create, modify, delete, consult
- **Prescriptions**: Add, view
- **Medical reports**: Create, modify, delete

### 🌐 REST Management
- **Appointments**: Schedule, view, cancel
- **Notifications**: Email sending (confirmation, modification)
- **Patient follow-up**: Consultation history, reports, status changes

### ⚙️ BPMN Orchestration
- Doctor availability verification
- Automatic record creation for new patients
- Automated email sending
- Follow-up updates after each consultation

<div align="right">
  <a href="#top">⬆ Back to top</a>
</div>

---

## Technologies Used<a name="tech"></a>

<div align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/SpringBoot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot">
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis">
</div>

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Java 8, Spring Boot 2.7
- **In-memory database**: Redis via Jedis
- **Business process**: Bonita BPM (BPMN)
- **API testing tools**: SOAPUI, Postman
- **Email simulation**: Mailtrap

---

## Architecture<a name="architecture"></a>
- **Config Package**: CORS & SMTP configurations
- **Jedis Package**: Shared data management between SOAP & REST
- **REST Package**: Controllers, services and models for appointments, notifications, follow-up
- **SOAP Package**: Entities, interfaces, implementations for records, patients, doctors, prescriptions
- **Application**: SOAP services (port 8080) and REST services (port 8081) launched together

<div align="right">
  <a href="#top">⬆ Back to top</a>
</div>

---

## Installation<a name="installation"></a>

### Prerequisites
- Java 8+
- Redis installed and configured
- Java IDE (IntelliJ / Eclipse)
- Bonita BPM (for BPMN process)

### Steps
1. **Install prerequisites** (Java, Redis, Bonita BPM)
2. **Launch Redis server**:
   ```bash
   redis-server
   ```
2. **Open Java project** in your IDE
3. **Start the application**
4. **Access frontend** locally via a browser
5. **Test** using:
   - **SOAPUI** for SOAP services
   - **Postman** for REST services

---

## Tests and Demonstrations<a name="demo"></a>
- **SOAPUI**: Testing SOAP operations (patients, doctors, prescriptions...)
- **Postman**: Testing REST endpoints (appointments, notifications, follow-up)
- **Frontend**: Simple forms to interact with services
- **Mailtrap**: Simulating confirmation email sending

---

## Future Improvements<a name="future"></a>
1. More ergonomic frontend interface (**React**, **Angular**)
2. Enhanced security (**JWT**, **OAuth2**)
3. **SMS** management in addition to emails
4. **Cloud deployment** (AWS, Azure)
5. Integration of a **persistent database** (MySQL/PostgreSQL)
6. **WebSocket** integration for real-time notifications

<div align="right">
  <a href="#top">⬆ Back to top</a>
</div>

---

## Application Demo<a name="app"></a>
<img src="image/1.png" style="width: 80%; max-width: 600px; height: auto; display: block; margin: 20px auto; border: 2px solid #ccc; border-radius: 10px;" alt="Appointment Scheduling Interface">
<img src="image/2.png" style="width: 80%; max-width: 600px; height: auto; display: block; margin: 20px auto; border: 2px solid #ccc; border-radius: 10px;" alt="Patient Management Dashboard">
<img src="image/3.png" style="width: 80%; max-width: 600px; height: auto; display: block; margin: 20px auto; border: 2px solid #ccc; border-radius: 10px;" alt="Medical Records View">
<img src="image/4.png" style="width: 80%; max-width: 600px; height: auto; display: block; margin: 20px auto; border: 2px solid #ccc; border-radius: 10px;" alt="Prescription Management">
<img src="image/5.png" style="width: 80%; max-width: 600px; height: auto; display: block; margin: 20px auto; border: 2px solid #ccc; border-radius: 10px;" alt="Doctor Availability Calendar">
<img src="image/6.png" style="width: 80%; max-width: 600px; height: auto; display: block; margin: 20px auto; border: 2px solid #ccc; border-radius: 10px;" alt="Notification System">
<img src="image/7.png" style="width: 80%; max-width: 600px; height: auto; display: block; margin: 20px auto; border: 2px solid #ccc; border-radius: 10px;" alt="Patient Follow-up Interface">
<img src="image/8.png" style="width: 80%; max-width: 600px; height: auto; display: block; margin: 20px auto; border: 2px solid #ccc; border-radius: 10px;" alt="BPMN Orchestration Workflow">
<img src="image/9.png" style="width: 80%; max-width: 600px; height: auto; display: block; margin: 20px auto; border: 2px solid #ccc; border-radius: 10px;" alt="Email Confirmation Preview">
<img src="image/10.png" style="width: 80%; max-width: 600px; height: auto; display: block; margin: 20px auto; border: 2px solid #ccc; border-radius: 10px;" alt="System Architecture Overview">

<div align="right">
  <a href="#top">⬆ Back to top</a>
</div>
