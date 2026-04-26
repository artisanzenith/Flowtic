# Flowtic Frontend (Next.js + Tailwind)

Modern SaaS frontend for chatbot automation, client workflow automation, and appointment orchestration.

## Tech Stack

- Next.js (App Router)
- TypeScript
- Tailwind CSS
- LocalStorage-based mock auth

## Run Locally

1. Install dependencies:
   ```bash
   npm install
   ```
2. Start dev server:
   ```bash
   npm run dev
   ```
3. Open `http://localhost:3000`

## Routes

- `/` - Marketing landing page
- `/login` - Login form
- `/signup` - Signup form
- `/dashboard` - Protected app dashboard

## Edit Content Quickly

- Landing sections:
  - `components/home/Hero.tsx`
  - `components/home/Features.tsx`
  - `components/home/HowItWorks.tsx`
  - `components/home/Pricing.tsx`
  - `components/home/Testimonials.tsx`
- Navbar/Footer:
  - `components/layout/Navbar.tsx`
  - `components/layout/Footer.tsx`
- Dashboard modules:
  - `app/dashboard/page.tsx`

## Backend Integration Later

- API layer placeholder:
  - `lib/api.ts`
- Auth state provider:
  - `context/AuthContext.tsx`

Replace mock methods in `lib/api.ts` with real API calls to your Node.js backend or Supabase.

## Smart Chatbot Setup (No Login Required)

The website includes a floating chatbot for all visitors:

- Auto opens after 5 seconds
- Works without user login
- Calls `POST /api/chat`

To enable smart AI replies:

1. Create `.env.local` in project root
2. Add:
   ```bash
   OPENAI_API_KEY=your_openai_api_key_here
   OPENAI_MODEL=gpt-4o-mini
   ```
3. Restart dev server
