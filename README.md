# securecorp-sso-app
A corporate-style React front-end page that integrates with Single Sign-On (SSO) using Microsoft Azure AD. The application checks a user's AD group with membership to control access to certain pages within the app.

## Tech Stack
- Frontend: React.js
- Backend: Python (FastAPI)
- Authentication Provider: Azure Active Directory

## Features
- Azure AD login via OAUTH 2.0
- Backend verifies token and checks AD group membership.
- React app shows/hides content based on role

## Folder Structure
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

## Authors
- [@JustinTurner](https://github.com/Turner-Justin)
