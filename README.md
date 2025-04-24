# securecorp-sso-app
A corporate-style React front-end page that integrates with Single Sign-On (SSO) using Microsoft Azure AD. The application checks a user's AD group with membership to control access to certain pages within the app.

## NOTE:
Microsoft has recently changed its process for granting access to the Microsoft 365 Developer Program. Given these constraints, I've decided to simulate SSO on my local host before moving this development project to a paid Azure AD plan. 
I hope to learn and practice:
- Logging in via a simulated SSO provider
- Receiving a JWT (simulating Azure AD)
- Backend verifies and decodes the JWT
- The backend checks group membership before returning protected data
- React protects pages based on group membership

## Architecture Overview:
```
Frontend (React) 
    ⬇️ login button
    ↪️ Redirects to Mock SSO login screen
        ⬆️ returns JWT (with group info)
    ⬇️ sends token to backend

Backend (FastAPI)
    ✔️ Verifies token signature
    🔍 Checks group membership
    ⬆️ Sends access or denial back to frontend

Frontend (React)
    ✅ Shows or hides pages based on response
```
## Tech Stack
- Frontend: React.js
- Backend: Python (FastAPI)
- Authentication Provider: Azure Active Directory

## Features
- Azure AD login via OAUTH 2.0
- Backend verifies token and checks AD group membership.
- React app shows/hides content based on role

## Folder Structure
```
securecorp-sso-app/
│
├── frontend/                 # React App
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── utils/
│   │   └── App.js
│   └── .env
│
├── backend/                  # Python Backend (FastAPI)
│   ├── main.py
│   ├── auth/
│   │   ├── azure_auth.py
│   │   └── group_check.py
│   └── requirements.txt
│
├── README.md
└── .gitignore
```

## Authors
- [@JustinTurner](https://github.com/Turner-Justin)
