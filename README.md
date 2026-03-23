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
npm run dev   # runs on port 3001

# Frontend
cd frontend
npm install
npm run dev   # runs on port 5173
```

---

## 🛠️ Open Test Task: Crypto Payment Gateway( 4h )

> **This is an open test development task.** The platform currently has Premium ($50) and Elite ($99) subscription plans with Pay buttons on the Subscription page, but no payment backend or admin system. We are looking for a developer to implement this end-to-end.

### What already exists

- User auth (signup, login, JWT)
- Subscription page with Premium / Elite Pay buttons
- Basic admin login page (no payment management yet)
- Supabase `users` table (no subscription columns yet)

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

Wallet address: `0xd4062e68022ef5235898CBc4f069A0df4fF2Ea6C`

Plan prices:
- Premium: **$50/month**
- Elite: **$99/month**

#### 4. Admin Panel

- Protected route — only accessible with admin credentials
- Table showing all payment requests (name, email, plan, chain, tx hash, status, date)
- Approve ✓ button — sets user `subscription_plan` and `subscription_expires_at` (+30 days) in DB
- Reject ✗ button — marks request as rejected

### Deliverables

- [ ] SQL migration file for new tables/columns
- [ ] Backend payment routes (`/api/payments/...`)
- [ ] Payment modal component (frontend)
- [ ] Admin panel with approve/reject
- [ ] README update with any new env variables
- [ ] **Live deployed URLs** — both frontend and backend must be deployed and working

### Deployment Requirements

- Frontend deployed on **Vercel** (or equivalent)
- Backend deployed on **Vercel / Railway / Render** (or equivalent)
- All environment variables configured on the hosting platform
- The full flow must work on the live site:
  1. User selects plan → clicks Pay
  2. Selects chain, sends crypto to wallet address
  3. Submits tx hash + name + email
  4. Admin logs in, sees the request
  5. Admin approves → user subscription activates
- **Do not submit localhost screenshots** — only live URL demos will be accepted

### Evaluation Criteria

- Clean, readable code
- Proper error handling on all endpoints
- Admin route is secure (not accessible to regular users)
- No hardcoded secrets or API keys
- Live site works without issues at time of review

---

## 📬 Submission

Please provide:
1. Link to your forked GitHub repository with the implementation
2. Live frontend URL
3. Live backend URL
4. Admin login credentials for review (temporary test account)
