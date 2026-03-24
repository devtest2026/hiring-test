# Trading Strategy Platform

A full-stack trading strategy platform built with React, Node.js, and Supabase.

## 🧱 Tech Stack

- **Frontend:** React, TypeScript, Vite, Tailwind CSS
- **Backend:** Node.js, Express, deployed on Vercel
- **Database:** Supabase (PostgreSQL)
- **Auth:** JWT-based login/signup

## 📁 Project Structure

```
/
├── frontend/          # React + Vite frontend
│   ├── src/
│   │   ├── pages/     # Route pages
│   │   ├── components/
│   │   └── lib/       # API helpers
│   └── .env.example
└── backend/           # Express API
    ├── src/
    │   ├── routes/
    │   ├── controllers/
    │   └── middleware/
    └── .env.example
```

## 🚀 Local Setup

```bash
# Backend
cd backend
npm install
npm start   # runs on port 3001

# Frontend
cd frontend
npm install
npm run dev   # runs on port 5173
```

---

## 🛠️ Open Test Task: Crypto Payment Gateway( 4h )

> **This is an open test development task.** The platform currently has Premium ($50) and Elite ($99) subscription plans with Pay buttons on the Subscription page, but no payment backend or admin system. We are looking for a developer to implement this end-to-end.

### What needs to be built

#### 1. Supabase Schema

Add the following to the database:

```sql
...
```

#### 2. Backend API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/payments/request` | User submits payment info |
| GET | `/api/payments/requests` | Admin fetches all requests |
| POST | `/api/payments/requests/:id/approve` | Admin approves, activates subscription |
| POST | `/api/payments/requests/:id/reject` | Admin rejects request |

#### 3. Payment Modal (Frontend)

When user clicks Pay on the Subscription page, show a modal with:

- **Step 1:** Chain selector (support at least 20 networks — Ethereum, BSC, Polygon, Arbitrum, Optimism, Avalanche, Solana, etc.)
- **Step 2:** Display our wallet address + QR code, form for user name, email, and transaction hash
- **Step 3:** Confirmation screen after submission

### Evaluation Criteria

| Area | Weight |
|------|--------|
| Code Quality & Architecture | 30% |
| Feature Implementation | 30% |
| Performance | 20% |
| User Experience | 10% |
| Unit Testing | 10% |

---

## 📬 Submission
Link to your forked GitHub repository with the implementation

**Live Preview:** [https://tradex.pumapulse.org](https://tradex.pumapulse.org)

---

## Success Criteria

Deliver a production-quality chart implementation that demonstrates senior-level skills in architecture, performance optimization, and user experience design.

---


_Maintained by [PumaPulse Org](https://pumapulse.org)_

