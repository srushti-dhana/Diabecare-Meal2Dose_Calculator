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
- **Encrypted Transport Layer:** All communication is encrypted (HTTPS).
- **No Hardcoded Secrets:** All keys stored server-side or in environment variables.

---

## 🏗️ Architecture

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/f5133681-e166-4b5f-bcf5-3f4a2d21ca12" />

---

## 🧰 Technology Stack

### **Frontend**
- React.js
- TypeScript
- Vite
- Tailwind CSS
- ShadCN UI
- Radix UI
- React Hook Form
- Zod
- Framer Motion

### **Backend**
- Supabase
- PostgreSQL
- Supabase Auth
- Supabase Edge Functions
- RLS Policies

### **APIs**
- CalorieNinjas API

---

## 📦 Getting Started

### **Prerequisites**
- Node.js (16+)
- Supabase Account
- CalorieNinjas API Key
- Git installed

---

## 🌍 Environment Variables

### **Frontend (`.env`)**
```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_anon_key
VITE_EDGE_FUNCTION_URL=your_edge_function_url
```

### **Supabase Edge Function (`.env`)**
```env
CALORIE_NINJA_API_KEY=your_api_key
```

---

## ⚙️ Installation

### **Clone the repository**
```bash
git clone <repo-url>
cd Meal2Dose
```

### **Install frontend dependencies**
```bash
npm install
```

### **Run the development server**
```bash
npm run dev
```

### **Deploy Supabase Edge Function**
```bash
supabase functions deploy fetch-nutrition
```

---

## 🧱 Project Structure
```
Meal2Dose/
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
```

---

## 🧪 Usage

### 1. **Sign Up / Log In**
Users create an account using Supabase Auth.

### 2. **Set Medical Parameters**
- Total Daily Dose (TDD)  
- Insulin-to-Carb Ratio (I:C)  
- Target Blood Glucose  

### 3. **Search for Food**
Supports Indian + international meals:  
Roti, Paratha, Idli, Dosa, Pasta, Rice, Sandwiches, Pizza, Sushi, Burgers, etc.

### 4. **Enter Quantity**
Food → Portion Size → Carb Calculation

### 5. **View Insulin Dose**
The app calculates:
- Carb-based insulin  
- Correction insulin  
- Total insulin units  

### 6. **Save the Dose History**
All records securely stored with RLS.

---

## 🛡️ Security Considerations

### Application Security
- No access without authentication  
- Strict RLS policies  
- Strong validation on client & server  

### API Security
- API keys hidden using Edge Functions  
- No exposure of sensitive keys  

### User Privacy
- Users can only view their own logs  
- No public data access  

---

## 📈 Future Enhancements
- 📸 AI food detection via camera  
- 🤖 ML-based insulin recommendations  
- 📱 Mobile app (Flutter / React Native)  
- 🩺 Doctor monitoring dashboard  
- ⌚ Smart glucometer integration  
- 🌐 Multi-language support  
- 🔔 Meal & insulin reminders  

---

## 🛠️ Deployment

### Local Development
```bash
npm install
npm run dev
supabase start
```

### Production Build
```bash
npm run build
```

### Production Deployment
- Deploy frontend to Netlify / Vercel  
- Deploy Supabase Edge Functions  
- Configure production `.env` files  

---

## 🤝 Contributing
1. Fork the repository  
2. Create a feature branch  
3. Make your changes  
4. Test thoroughly  
5. Submit a Pull Request  

---

Made with ❤️ by **Srushti Dhanawade**

