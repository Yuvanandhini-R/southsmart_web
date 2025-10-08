
# SOUTHSMART WEBSITE AND ADMIN PANEL

This repository is for the official **Southsmart Technologies** website and its secure administrative control panel. The platform connects clients with reliable equipment and support services, featuring a dynamic, modern, and interactive user interface.

---

## 🚀 Overview

The Southsmart platform is a modern, single-page application built with **React** and powered by a scalable **Firebase** backend.

### Key Features

- **Public Website:** Three main pages (About, Equipment, Assistance) with interactive content.  
- **Dynamic UI/UX:** **Three.js** for a 3D hero section and **AOS** for smooth scroll animations.  
- **Smart Navigation:** Cross-page search functionality for seamless experience.  
- **Secure Admin Panel:** Managed via Firebase Authentication for user queries, equipment data, and customer conversions.  
- **Email Automation:** Firebase Cloud Functions and NodeMailer handle form submissions and notifications.  

---

## 🛠️ Technology Stack

| Category         | Technology                                | Purpose                                                      |
|-----------------|------------------------------------------|-------------------------------------------------------------|
| **Frontend**     | React                                     | Core UI library                                             |
| **Styling**      | Tailwind CSS                              | Responsive, utility-first design framework                  |
| **3D/Animation** | Three.js, Framer Motion, GSAP, AOS       | Dynamic, immersive visuals                                   |
| **Database**     | Firebase Firestore                        | Real-time, structured NoSQL storage                          |
| **Backend**      | Firebase Cloud Functions                  | Serverless logic for form handling & email services         |
| **Auth/Hosting** | Firebase Authentication, Firebase Hosting | Admin access control and scalable deployment infrastructure |
| **Build Tool**   | Vite                                      | Fast development server and build tool                      |

---

## ⚙️ Installation Guide

### Prerequisites

- Node.js (v18 or higher)  
- npm (comes with Node.js)  
- Git  
- Firebase CLI: `npm install -g firebase-tools`  
- A Google Firebase account with an active project  

### Step 1: Clone the Repository

```bash
cd path/to/your/projects/folder
git clone https://github.com/your-username/southsmart-web.git
cd southsmart-web
```

### Step 2: Install Dependencies

```bash
npm install
```

### Step 3: Configure Firebase

1. Login to Firebase:  
```bash
firebase login
```

2. Initialize / Link Project:  
```bash
firebase init
```  
*(Follow prompts to set up Hosting, Functions, and Firestore.)*

3. Update `firebaseConfig.js` (frontend):  
```javascript
const firebaseConfig = {
  apiKey: "your_api_key",
  authDomain: "your_project.firebaseapp.com",
  projectId: "your_project_id",
  // ...other credentials
};
```

4. Backend Functions: Securely configure SMTP credentials using Firebase environment variables.  
⚠️ **Do not hardcode sensitive credentials in production.**

---

### ▶️ Running the Application

**Frontend (React Development Server):**  
```bash
npm run dev
```

**Backend (Firebase Emulators for Functions & Firestore):**  
```bash
firebase emulators:start
```

---

### ☁️ Deployment

**Build Production Assets:**  
```bash
npm run build
```

**Deploy to Firebase Hosting & Functions:**  
```bash
firebase deploy
```

---

## 📝 Admin Panel Usage & API

**Data Flow (Firestore Collections):**

- `ssmartquery`: Initial user submissions  
- `enquiries`: Admin-reviewed entries for follow-up  
- `customers`: Confirmed clients  

**Conversion Actions:**

1. **Query → Enquiry:** Triggers follow-up email.  
2. **Enquiry → Customer:** Finalizes client relationship.  
3. **Rollback:** Revert conversions (Customer → Enquiry).  

All conversions are handled via protected Firebase Cloud Functions with automated NodeMailer emails.

---

## 🤝 Support and Contribution

**For Issues:** Refer to the TECHNICAL DOCUMENT included in the repository.  

**Contributing Guidelines:**

1. Fork the repository.  
2. Create your feature branch: `git checkout -b feature/AmazingFeature`  
3. Commit changes: `git commit -m 'Add some AmazingFeature'`  
4. Push branch: `git push origin feature/AmazingFeature`  
5. Open a Pull Request.  

---
