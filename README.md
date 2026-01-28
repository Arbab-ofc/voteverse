# VoteVerse v2

![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-7-646CFF?logo=vite&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4-38B2AC?logo=tailwindcss&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-20-339933?logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-5-000000?logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-8-47A248?logo=mongodb&logoColor=white)
![Socket.IO](https://img.shields.io/badge/Socket.IO-4-010101?logo=socket.io&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-Admin-FFCA28?logo=firebase&logoColor=black)
![Vercel](https://img.shields.io/badge/Vercel-Frontend-000000?logo=vercel&logoColor=white)
![Render](https://img.shields.io/badge/Render-Backend-5A67D8?logo=render&logoColor=white)

> VoteVerse v2 (second version) is a fullstack online voting platform with secure auth, election management, and real-time participation.

---

## Repositories

This project is split into two repos:

- **Client**: `voteverse-client`
- **Server**: `voteverse-server`

This workspace contains both for local development convenience.

---

## Highlights

- Versioned API (`/api/v2`)
- JWT cookie authentication + OTP verification
- Google sign-in (Firebase Admin)
- Election, candidate, vote, and audit logs
- Real-time updates with Socket.IO
- Polished UI with motion and responsive layouts

---

## Architecture

Client (React) → REST + Socket.IO → Server (Express) → MongoDB

---

## Quick Start (Local)

```bash
git clone https://github.com/Arbab-ofc/voteverse-client.git
git clone https://github.com/Arbab-ofc/voteverse-server.git
```

### Client

```bash
cd voteverse-client
npm install
npm run dev
```

### Server

```bash
cd voteverse-server
npm install
npm run dev
```

---

## Environment Variables

### Client (`client/.env`)

```
VITE_API_URL=https://api.voteverse.pw
VITE_SOCKET_URL=https://api.voteverse.pw
```

### Server (`server/.env`)

```
PORT=5000
MONGO_URI=your_mongo_connection_string
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_email@example.com
EMAIL_PASS=your_email_password
CLIENT_URL=https://www.voteverse.pw
FIREBASE_PROJECT_ID=your_firebase_project_id
FIREBASE_CLIENT_EMAIL=your_firebase_client_email
FIREBASE_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\n...\n-----END PRIVATE KEY-----\n"
```

---

## API Endpoints (v2)

Base: `/api/v2`

### Auth & Users (`/users`)
- `POST /users/register` — Register user + send OTP
- `POST /users/login` — Email/password login
- `POST /users/google-login` — Google login (Firebase)
- `POST /users/verify-otp` — Verify OTP
- `POST /users/resend-otp` — Resend OTP
- `POST /users/forget` — Start password reset (send OTP)
- `POST /users/reset-password` — Reset password with OTP
- `PUT /users/change-password` — Change password (auth)
- `GET /users/profile` — Current user profile (auth)
- `POST /users/logout` — Logout (auth)

### Elections (`/elections`)
- `POST /elections/create-election` — Create election (auth)
- `GET /elections/all` — All elections (auth)
- `GET /elections/id/:id` — Election by id (auth)
- `PUT /elections/:id` — Update election (auth)
- `DELETE /elections/:id` — Delete election (auth)
- `GET /elections/my` — Elections created by user (auth)
- `GET /elections/result/:id` — Election results (auth)
- `PUT /elections/end/:id` — End election (auth)
- `POST /elections/:id/candidates` — Add candidate to election (auth)
- `DELETE /elections/:id/candidates/:candidateId` — Remove candidate (auth)

### Candidates (`/candidates`)
- `GET /candidates/election/:electionId` — Candidates by election (auth)
- `POST /candidates/add-candidate` — Create candidate (auth)

### Votes (`/votes`)
- `POST /votes/vote-candidate` — Cast vote (auth)
- `GET /votes/election/:electionId` — Votes by election (auth)

### Voter Logs (`/voter-logs`)
- `POST /voter-logs` — Log voter activity (auth)
- `GET /voter-logs/election/:electionId` — Logs by election (auth)

### Contact (`/contact`)
- `POST /contact` — Submit contact form

### Admin (`/admin`) (auth + admin)
- `GET /admin/users` — List users
- `PATCH /admin/users/:id/verify` — Verify user
- `PATCH /admin/users/:id/promote` — Promote user to admin
- `DELETE /admin/users/:id` — Delete user
- `GET /admin/elections` — List elections
- `DELETE /admin/elections/:id` — Delete election
- `GET /admin/contact-messages` — List contact messages
- `DELETE /admin/contact-messages/:id` — Delete contact message

### Public (`/public`)
- `GET /public/elections/id/:id` — Public election view

---

## Deployment

- **Client**: Vercel
- **Server**: Render

Make sure `CLIENT_URL` matches the deployed frontend domain.

---

## Screenshots

![Home Page](client/src/assets/homePage.png)
![Login Page](client/src/assets/loginPage.png)
![Register Page](client/src/assets/registerPage.png)
![Election Page](client/src/assets/electionPage.png)
![Vote Page](client/src/assets/votePage.png)
![Not Found Page](client/src/assets/notFound.png)
