<div align="center">

<img src="banner.png" alt="HealthSync: one app for patients, doctors and hospital staff" width="100%">

# HealthSync

**A hospital communication app for Android that connects patients, doctors, hospital staff and admins in one place.**

Designed and developed by **[Hassaan](https://github.com/hassaan2077)**

![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![React Native](https://img.shields.io/badge/React_Native_0.76-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Cloudflare Workers](https://img.shields.io/badge/Cloudflare_Workers-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)

### 🌐 [Visit the website →](https://hassaan2077.github.io/HealthSync-Showcase/)

[Highlights](#highlights) · [Screenshots](#screenshots) · [Features](#features) · [Security](#security-and-privacy) · [Architecture](#architecture) · [Tech stack](#tech-stack)

</div>

---

## Highlights

- 👥 **Four roles, four dashboards:** Patient, Doctor, Hospital Staff (10 staff roles) and Admin
- 💬 **Real-time chat and video calls**, with voice notes, files, read receipts and push notifications
- 📋 **Clinical task routing:** doctors send tasks to any of 15 hospital departments or to named staff; the first person to complete a task claims it
- 📝 **Patient health notes** that patients share with a doctor, who replies with comments
- 🧠 **AI brain MRI analysis:** tumour classification, a Grad-CAM heatmap and a PDF report
- 🤖 **AI health assistant** that answers medical questions in a clear, structured way
- 🔐 **Secure by design:** per-user database rules, no secret keys inside the app, admin-only admin creation

---

## Screenshots

> Screens are from the app running on a real Android phone. Names, emails and other personal details are blurred.

### Getting started

<table>
  <tr>
    <td align="center"><img src="screenshots/01-splash.png" width="200"><br><sub><b>Intro screen</b></sub></td>
    <td align="center"><img src="screenshots/02-welcome.png" width="200"><br><sub><b>Welcome</b></sub></td>
    <td align="center"><img src="screenshots/03-choose-role.png" width="200"><br><sub><b>Choose your role</b></sub></td>
    <td align="center"><img src="screenshots/04-login.png" width="200"><br><sub><b>Login</b></sub></td>
  </tr>
  <tr>
    <td align="center"><img src="screenshots/05-patient-signup.png" width="200"><br><sub><b>Patient sign-up (email or phone OTP)</b></sub></td>
    <td align="center"><img src="screenshots/06-staff-signup.png" width="200"><br><sub><b>Hospital staff sign-up</b></sub></td>
    <td align="center"><img src="screenshots/12-health-notes.png" width="200"><br><sub><b>Patient health notes</b></sub></td>
    <td align="center"><img src="screenshots/13-settings.png" width="200"><br><sub><b>Fingerprint login and account settings</b></sub></td>
  </tr>
</table>

### Doctors and clinical tasks

<table>
  <tr>
    <td align="center"><img src="screenshots/07-doctor-home.png" width="200"><br><sub><b>Doctor dashboard</b></sub></td>
    <td align="center"><img src="screenshots/08-create-task.png" width="200"><br><sub><b>Create and route a task</b></sub></td>
    <td align="center"><img src="screenshots/09-task-history.png" width="200"><br><sub><b>Completed task history</b></sub></td>
    <td align="center"><img src="screenshots/14-staff-tasks.png" width="200"><br><sub><b>Staff task inbox</b></sub></td>
  </tr>
</table>

### Messaging and video calls

<table>
  <tr>
    <td align="center"><img src="screenshots/10-messages.png" width="200"><br><sub><b>Conversations</b></sub></td>
    <td align="center"><img src="screenshots/11-chat-health-note.png" width="200"><br><sub><b>Health note shared in chat</b></sub></td>
    <td align="center"><img src="screenshots/15-voice-note.png" width="200"><br><sub><b>Voice notes and read receipts</b></sub></td>
    <td align="center"><img src="screenshots/16-video-call.png" width="200"><br><sub><b>Video call</b></sub></td>
  </tr>
</table>

### Admin

<table>
  <tr>
    <td align="center"><img src="screenshots/17-admin-home.png" width="200"><br><sub><b>Admin dashboard</b></sub></td>
    <td align="center"><img src="screenshots/18-new-admin.png" width="200"><br><sub><b>Create a new admin</b></sub></td>
    <td align="center"><img src="screenshots/19-admin-directory.png" width="200"><br><sub><b>Team and patient directory</b></sub></td>
  </tr>
</table>

---

## Features

### 🧑 For patients
- **Health notes:** a personal health journal, searchable by day or date
- **Share with a doctor:** send one note to a chosen doctor, who can reply with comments that appear on the note and in the chat
- **Chat and video calls** with doctors and staff
- **AI health assistant:** ask medical questions and get structured answers (overview, key facts, when to see a doctor, treatment options)
- **Sign up with email or phone number** (OTP), and reset a forgotten password by OTP

### 🩺 For doctors
- **Clinical tasks:** create tasks for a patient with priority and notes, and route them to a department or to specific staff members
- **Live tracking** of incomplete and completed tasks, with in-app and push notifications when staff complete them
- **Review shared health notes** and reply in context
- **Messaging and video calls** with patients and colleagues

### 🏥 For hospital staff
- **Task inbox** for the staff member's department or tasks assigned to them; the first to tap *Complete* claims the task
- **10 staff roles** (nurses, medical officers, physiotherapists, lab staff and more) across **15 departments**
- **AI brain MRI analysis** for lab staff: upload a scan and get a classification (glioma, meningioma, pituitary tumour or no tumour), a Grad-CAM heatmap of what the model looked at, and a PDF report

### 🛡️ For admins
- **Team and patient directory** with search, filters and on-call status
- **Create new admins** from inside the app; nobody can sign up as an admin

### ✨ Across the app
- Push notifications that arrive whether the app is open, in the background or closed, and open the right screen when tapped
- Fingerprint login backed by the device keystore
- Email verification before first login
- Account deactivation, reactivation and deletion
- Clean, consistent design with the Poppins typeface and a layout that scales to every screen size

---

## Security and privacy

Health data needs care, so HealthSync was built and reviewed with security in mind:

| Area | How it's handled |
|---|---|
| **Database access** | Firebase security rules let each person read only their own chats and health notes. Tasks are visible only to hospital staff. |
| **Secret keys** | No secret key ships inside the app. Push notifications go through a small serverless service on Cloudflare that holds the key and checks the sender's login first. |
| **Roles** | Users can't make themselves admins. Only an existing admin can create a new one, and the database rules enforce this. |
| **Accounts** | Email accounts must be verified before first login; phone accounts are verified by OTP. |
| **Credentials on device** | Sessions and fingerprint-login details are kept in encrypted storage and the Android keystore. |

---

## Architecture

```mermaid
flowchart LR
    App["📱 HealthSync app<br/>React Native · Android"]
    App -- "Login, chat, notes, tasks" --> Firebase[("🔥 Firebase<br/>Auth + Realtime Database")]
    App -- "Send notification" --> Worker["☁️ Push service<br/>Cloudflare Worker"]
    Worker -- "Verify sender, find device" --> Firebase
    Worker -- "Deliver" --> FCM["🔔 Firebase Cloud Messaging"]
    App -- "Video calls" --> Zego["🎥 ZEGOCLOUD"]
    App -- "MRI scan" --> MRI["🧠 MRI service<br/>Flask + PyTorch"]
    App -- "Medical question" --> Bot["🤖 Assistant service<br/>Flask"]
    Bot --> HF["Hugging Face models"]
```

---

## Tech stack

| Layer | Technology |
|---|---|
| Mobile app | React Native 0.76 (New Architecture, Hermes), React Navigation, Lottie, Reanimated |
| Backend | Firebase Authentication, Realtime Database and Cloud Messaging |
| Push service | Cloudflare Workers (serverless) |
| Video calls | ZEGOCLOUD |
| AI: MRI analysis | Python, Flask, PyTorch (MobileNetV3 with attention), Grad-CAM, PDF reports |
| AI: assistant | Python, Flask, Hugging Face Inference (Mistral 7B, with fallbacks) |
| Security | Firebase security rules, encrypted storage, Android keystore biometrics |

---

## About this repository

This repository is a **public showcase** of HealthSync. The source code is kept in a private repository. If you'd like to see the code or talk about the project, contact me through GitHub.

<div align="center">

### 👨‍💻 Developed by Hassaan

[![GitHub](https://img.shields.io/badge/GitHub-hassaan2077-181717?style=for-the-badge&logo=github)](https://github.com/hassaan2077)

<sub>© 2026 Hassaan. All rights reserved.</sub>

</div>
