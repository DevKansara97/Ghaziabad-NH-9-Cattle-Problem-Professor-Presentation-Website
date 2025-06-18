# Ghaziabad NH9 Cattle Problem - Prompt Engineering Game

An interactive web-based application designed to enhance prompt engineering skills by simulating a real-world problem. Students formulate AI prompts, and a professor evaluates them, observing the (conceptual) impact on a simulated environment.

Developed by **Dev Kansara** during an internship under **Prof. Suresh Malodia**.

## Table of Contents

1.  [Introduction](#1-introduction)
2.  [Features](#2-features)
3.  [Technologies Used](#3-technologies-used)
4.  [Project Structure](#4-project-structure)
5.  [Setup and Deployment](#5-setup-and-deployment)
    * [Prerequisites](#prerequisites)
    * [Firebase Project Setup](#firebase-project-setup)
    * [Code Configuration](#code-configuration)
    * [Deployment (e.g., Netlify)](#deployment-eg-netlify)
6.  [Usage](#6-usage)
7.  [Credits](#7-credits)

---

## 1. Introduction

This project is an educational game simulating the "Ghaziabad NH9 Cattle Problem" to teach **prompt engineering**. Students craft AI prompts to solve the issue of stray cattle, while a professor evaluates these prompts and their conceptual impact on a simple simulation. It features real-time data synchronization across multiple devices, achieved using Firebase Firestore.

## 2. Features

### 2.1. Student Interface (`student.html`)
* **Prompt Submission**: Input AI prompts with a Team ID (e.g., `team1`-`team6`).
* **Convenience**: "Copy My Prompt" feature and user-friendly modals.
* **Local Persistence**: Remembers the last used Team ID.

### 2.2. Professor Interface (`professor.html`)
* **Real-time Dashboard**: View all submitted prompts in real-time.
* **Prompt Evaluation**: Click to view a prompt and assign a rating (1-10).
* **Data Management**: "Clear All Prompts" button to reset the database.
* **Simulation View**: Integrated `simulation.html` for visual context.

### 2.3. Real-time Synchronization
* Uses **Firebase Firestore** for instant data updates across all connected devices (student submissions appear live on professor's dashboard, ratings update immediately).

### 2.4. Team Management
* Supports 2 to 6 teams using simple `teamX` IDs.

## 3. Technologies Used

* **HTML5**: Web page structure.
* **CSS3**: Styling and responsive design.
* **JavaScript (ES6+)**: Client-side logic and interactivity.
* **Firebase**:
    * **Firebase Authentication (Anonymous)**: Basic user identification.
    * **Cloud Firestore**: Real-time NoSQL cloud database for data storage and synchronization.

## 4. Project Structure
```
├── index.html          # Landing page (if you choose to implement one)
├── student.html        # Student's prompt submission interface
├── professor.html      # Professor's dashboard for evaluation
└── simulation.html     # Static HTML for the cattle simulation (embedded in professor.html)
└── README.md           # This file
```

## 5. Setup and Deployment

This application requires a Firebase project for real-time data synchronization.

### Prerequisites
* Google Account.
* Basic Git/GitHub understanding (for Netlify deployment).

### Firebase Project Setup

1.  **Create Project**: Go to [Firebase Console](https://console.firebase.google.com/), click "Add project."
2.  **Register Web App**: Add a web app and **copy your `firebaseConfig` object**.
3.  **Enable Anonymous Auth**: In Firebase Console > Authentication > Sign-in method, enable **"Anonymous"**.
4.  **Setup Firestore**: In Firebase Console > Firestore Database, click "Create database," choose **"Start in test mode,"** and select a data location.

### Code Configuration

1.  **Update HTML**: In both `student.html` and `professor.html`, locate the `firebaseConfig` JavaScript object and **replace the placeholder with your copied Firebase config**.

### Deployment (e.g., Netlify)

1.  **Version Control**: Commit and push all project files (`.html`, `.css`, etc.) to a GitHub repository.
2.  **Netlify Setup**: Log in to Netlify, create a "New site from Git," connect to your repository, and deploy.

## 6. Usage

1.  **Student Portal**: Open `student.html` (e.g., `your-netlify-app.netlify.app/student.html`) on student devices. Enter a Team ID and prompt, then click "Submit Prompt."
2.  **Professor Portal**: Open `professor.html` (e.g., `your-netlify-app.netlify.app/professor.html`) on the professor's device. Prompts appear in real-time. Click to view and rate, or use "Clear All Prompts" to reset data.

## 7. Credits

* **Developed by:** Dev Kansara
* **Internship Mentor:** Prof. Suresh Malodia
* **Intermediate Communicator:** Anmol Trivedi

Special thanks to Prof. Suresh Malodia for the valuable guidance and Anmol Trivedi for facilitating communication during this engaging project.
