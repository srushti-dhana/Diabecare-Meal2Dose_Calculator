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


