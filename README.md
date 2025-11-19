# 🍽️ Meal2Dose – Intelligent Insulin Dose Calculator

A smart, privacy-focused platform that calculates personalized insulin doses for diabetic users based on Indian and International foods. Built using **React**, **TypeScript**, **Tailwind**, **Supabase**, and secure serverless functions, Meal2Dose provides precise, data-driven insulin recommendations for everyday meals.

---

## ⭐ Features

### Core Functionality
- **Food-Based Insulin Calculator:** Automatically computes insulin dose using food carbs, user’s I:C ratio, TDD, and correction factor.  
- **Indian + Foreign Dishes Support:** Roti, idli, dosa, dal, pasta, noodles, soups, burgers, rice bowls, etc.  
- **Secure User Profiles:** Stores medical parameters such as Target BG, TDD, and insulin-carb ratio.  
- **Dose History Tracking:** Complete logging of previous meals, carb values, and insulin doses.  
- **Nutrition Lookup:** Uses CalorieNinjas API via Supabase Edge Functions.

### User Interface
- **Modern React UI:** Clean, responsive design with Tailwind + ShadCN components.  
- **Real-time Form Validation:** React Hook Form + Zod.  
- **Smooth Animations:** Integrated with Framer Motion.  
- **Dark/Light Theme Compatible:** Mobile-friendly and accessible.

---

## 🔐 Security Features
- **Supabase Authentication:** Secure signup, login, and session management.  
- **Row-Level Security (RLS):** Ensures users can only access their own medical data & dose logs.  
- **Edge Function API Proxy:** Protects external API keys by restricting direct frontend access.  
- **Encrypted Transport Layer:** All communication between client ↔ backend uses HTTPS.  
- **No Hardcoded Secrets:** All keys are server-side or environment-based.

---

## 🏗️ Architecture

### System Architecture

#### Frontend (React + TypeScript)
- React.js (Vite-based project setup)  
- TypeScript for safer type-checking  
- Tailwind CSS for utility-first responsiveness  
- ShadCN UI & Radix for accessible components  
- React Hook Form + Zod for validations  
- Framer Motion for UI animations

#### Backend (Supabase)
- Supabase Authentication  
- PostgreSQL Database  
- Edge Functions for secure API calls  
- Row Level Security (RLS)  
- Policies for per-user data isolation

#### External APIs
- **CalorieNinjas** for nutrition data  
- Accessed via Edge Function → API key protected

---

## 🧰 Technology Stack

### Frontend
- React.js  
- TypeScript  
- Vite  
- Tailwind CSS  
- ShadCN UI  
- Radix UI  
- React Hook Form  
- Zod  
- Framer Motion

### Backend
- Supabase  
- PostgreSQL  
- Supabase Auth  
- Supabase Edge Functions  
- RLS Policies

### APIs
- CalorieNinjas API (nutrition lookup)

---

## 📦 Getting Started

### Prerequisites
- Node.js (16+)  
- Supabase Account  
- CalorieNinjas API Key  
- Git

### Environment Variables

#### Frontend (`.env`)
```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_anon_key
VITE_EDGE_FUNCTION_URL=your_edge_function_url

## Supabase Edge Function (.env)
```env
CALORIE_NINJA_API_KEY=your_api_key

⚙️ Installation
Clone the repository
git clone <repo-url>
cd Meal2Dose

Install frontend dependencies
npm install

Run the development server
npm run dev

Deploy Supabase Edge Function
supabase functions deploy fetch-nutrition

🧱 Project Structure
.
├── src/
│   ├── components/
│   ├── pages/
│   ├── hooks/
│   ├── utils/
│   └── styles/
├── supabase/
│   ├── functions/
│   ├── migrations/
│   └── policies/
└── README.md

🧪 Usage
1. Sign Up / Log In

Users create an account using Supabase Auth.

2. Set Medical Parameters

Total Daily Dose (TDD)

Insulin-to-Carb Ratio (I:C)

Target Blood Glucose

3. Search for Food

Search Indian or foreign meals:

Roti, Paratha

Idli, Dosa

Pasta, Rice, Sandwiches

Pizza, Sushi, Burgers

4. Enter Quantity

Food → Portion Size → Carb Calculation

5. View Insulin Dose

The app calculates:

Carb-based insulin

Correction insulin

Total insulin units

6. Save the Dose History

All records stored securely in Supabase with RLS.

🛡️ Security Considerations
Application Security

No medical data stored without authentication

Strict RLS rules

Strong validation on both client & server side

API Security

API keys hidden using Edge Functions

Database protected with Policy-based access

User Privacy

Users can only access their own logs

No sharing or public access

📈 Future Enhancements

📸 AI food detection via camera

🤖 ML-based insulin recommendations

📱 Mobile app using Flutter or React Native

🩺 Doctor dashboard for monitoring

⌚ Integration with smart glucometers

🌐 Multi-language support

🔔 Reminders & notifications

🛠️ Deployment
Local Development
npm install
npm run dev
supabase start

Production Build
npm run build

Production Deployment

Deploy frontend to Netlify / Vercel

Deploy Supabase Edge Functions

Configure production .env files

🤝 Contributing

Fork the repository

Create a feature branch

Make changes

Test thoroughly

Submit a PR
