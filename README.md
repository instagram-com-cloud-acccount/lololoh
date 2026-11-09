# Vercel Message Demo

This is a minimal Next.js App Router demo containing:

- `app/api/messages/route.js` — accepts `POST /api/messages` with JSON `{ "message": "..." }`.
- `app/page.js` — a clearly labeled Security Testing Demo page with an explicit submit action.

## Install / deploy

1. Copy the `app` directory into your existing Next.js App Router project.
2. Ensure the project has a standard Next.js setup (`next`, `react`, and `react-dom`).
3. Run locally with `npm run dev`.
4. Deploy the project to Vercel.

The endpoint will be available at:

`https://YOUR-DEPLOYMENT.vercel.app/api/messages`

## Test

```bash
curl -X POST http://localhost:3000/api/messages \
  -H "Content-Type: application/json" \
  -d '{"message":"Hello from the demo"}'
```

## Storage note

This demo writes submitted messages to Vercel Function runtime logs using
`console.info`. Runtime logs are not a permanent database. Add a database only
if persistent storage is required, and provide an appropriate privacy notice.

Do not collect passwords, authentication tokens, or other sensitive data.
