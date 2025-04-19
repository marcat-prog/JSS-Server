[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/R98JjKZL)
﻿![](http://images.restapi.co.za/pvt/Noroff-64.png)
# Noroff
# Back-end Development Year 1
### JavaScript Server - Course Assignment 1 <sup>V2</sup>

Startup code for Noroff back-end development 1 - JavaScript Server course.

Instruction for the course assignment is in the LMS (Moodle) system of Noroff.
[https://lms.noroff.no](https://lms.noroff.no)

![](http://images.restapi.co .za/pvt/ca_important.png)

You will not be able to make any submission after the deadline of the course assignment. Make sure to make all your commit **BEFORE** the deadline

![](http://images.restapi.co.za/pvt/help.png)

If you are unsure of any instructions for the course assignment, contact out to your teacher on **Microsoft Teams**.

**REMEMBER** Your Moodle LMS submission must have your repository link **AND** your Github username in the text file.

# Meme Web Application

A simple web application for browsing memes, built with **Node.js**, **Express**, and **EJS**. Users can view memes, search, and view meme details — but only after logging in. Guests have limited access. The application uses **PassportJS** for authentication and tracks viewed memes using sessions and localStorage.

---

## 📦 Technologies Used

### Backend
- **Node.js**
- **Express**
- **EJS** (template engine)
- **PassportJS** (authentication)
- **express-session** (for session management)
- **axios** (to fetch meme data from an external API)

### Frontend
- **Bootstrap 5.2.3** (installed via NPM)
- **jQuery** (installed via NPM)
- **Custom CSS/JS** in `/public/css/` and `/public/js/`

---

## 🔐 Authentication

- User login system implemented using **Passport Local Strategy**
- Users are stored in `users.json` (contains 3 sample users)
- Passwords are stored in plaintext for development simplicity (can be hashed using bcrypt)

---

## 🔧 Installation Instructions

### 1. Clone the repository

```bash
git clone https://github.com/your-username/meme-app.git
cd meme-app

2. Install dependencies

npm install

This will install the following key dependencies:

express
ejs
passport
passport-local
express-session
axios
jquery
bootstrap@5.2.3

3. Folder Structure

/routes            -> Express routes
/views             -> EJS templates
/public/css        -> Custom CSS files
/public/js         -> Custom JS (like localStorage logic)
users.json         -> Stores user login data
config.json        -> Stores external API URL
app.js             -> Main server file

🚀 How to Run the App

Start the application with:

node app.js

Then visit:

http://localhost:3000

    ✅ No need for live-server. This is a full Express.js app and runs on its own.

👥 User Access
Role	Access
Guest	View memes (no details)
Logged-in	View meme details

Sample user accounts (users.json):

[
  {
    "id": 1 ,
    "username": "Josh",
    "password": "Josh1"
  },
  {
    "id": 2,
    "username": "FJ",
    "password": "FJ1"
  },
  {
    "id": 3,
    "username": "Student",
    "password": "Student1"
  }
]

📌 Notes

    Viewed memes are tracked via:

        localStorage in browser (visual highlight)

        req.session.viewedMemes in server (can be used for logic)

    All libraries are installed via NPM, no CDNs are used.