# PayApp Frontend (React + Vite + Tailwind)

A minimal, production-ready React frontend aligned with your Paytm-style backend.

## Quick Start
```bash
npm i
npm run dev
```

The app expects your backend at `http://localhost:3000/api/v1`.
- Signup: `POST /user/signup` → returns `{ token, ... }`
- Login:  `POST /user/login`   → returns `{ token, ... }` (add this in your backend if missing)
- Balance: `GET /accounts/balance` (header: `token: Bearer <jwt>`)
- Transfer: `POST /accounts/transfer` (header: `token: Bearer <jwt>`, body: `{ amount, to }`)

## Build
```bash
npm run build
npm run preview
```

## Notes
- Uses `lucide-react` for icons and `react-router-dom` v6 for routing.
- TailwindCSS is pre-configured.
- If your backend uses `Authorization: Bearer <token>` instead of `token: Bearer <token>`, update the headers in `src/App.jsx` accordingly.
