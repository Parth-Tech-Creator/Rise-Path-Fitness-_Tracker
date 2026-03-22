# 🏃‍♂️ RisePath Fitness Tracker
 
> Your complete fitness operating system — smart workouts, personalised nutrition, real-time step tracking, BMI calculator, and a built-in AI coach. All in a **single HTML file**. No installation. No backend. No internet required.
 
---
 
## 🚀 Features
 
- 🏋️ **6-Day Workout Split** — 8 exercises per day, complete any 5, with timestamps and progress bars
- 🥗 **7-Day Diet Plans** — Veg & Non-Veg with full macros, including Sunday Recovery meals
- 🔄 **Regenerate Meals** — Customise your plan by cuisine, calories, focus, and allergies
- 👣 **Step Counter** — Real accelerometer sensor on mobile + manual buttons on desktop
- 💧 **Hydration Tracker** — Log glasses with timestamps and 45-minute reminders
- ⚖️ **BMI Calculator** — Metric & Imperial, body fat %, ideal weight, personalised advice
- 🤖 **Built-in AI Coach** — Answers 20+ fitness topics offline with your personal stats
- 📊 **Live Dashboard** — All stats update in real time as you log activity
- 📈 **Progress & Achievements** — Weight trend chart + 6 unlockable achievements
- 🔐 **Auth System** — Sign Up, Login, Forgot Password — all stored in localStorage
- ⚙️ **Settings** — Edit profile, goal, activity level, password, and daily targets
- 🌙 **Daily Quotes** — 31 rotating motivational quotes, one per day of the month
 
---
 
## 🛠️ Tech Stack
 
| Layer | Technology |
|-------|-----------|
| Structure | HTML5 |
| Styling | CSS3 — custom properties, grid, flexbox, keyframe animations |
| Logic | Vanilla JavaScript (ES6+) — no frameworks |
| Fonts | Google Fonts — Inter, Bebas Neue, Space Mono |
| Storage | Browser `localStorage` — no server, no database |
| Motion API | `DeviceMotionEvent` — step tracking on mobile |
| Build Tools | None — just open the file |
 
---
 
## 📁 Project Structure
 
```
RisePath-Fitness-Tracker/
│
├── RisePath.html          ← Entire app (single file, ~590 KB)
├── README.md              ← This file
└── RisePath.png           ← App logo (also embedded as base64 in HTML)
```
 
> Everything — HTML, CSS, JavaScript, logo, meal data, workout data — lives inside one file.
 
---
 
## ⚙️ Installation & Setup
 
1. Clone the repository:
```bash
git clone https://github.com/Parth-Tech-Creator/Rise-Path-Fitness-_Tracker.git
```
 
2. Navigate to the project folder:
```bash
cd RisePath-Fitness-Tracker
```
 
3. Open `RisePath.html` in your browser — that's it. No `npm install`, no build step, no server needed.
 
> **Tip:** Works best in Chrome or Firefox. For step tracking on mobile, allow motion sensor permission when prompted.
 
---
 
## 📱 How It Works
 
```
Landing Page → Sign Up → Profile Setup (3 steps) → Home → Dashboard
```
 
1. **Sign Up** — Enter name, email, password (min 8 characters)
2. **Profile Setup** — Height, weight, age, gender → Activity level → Fitness goal
3. **Home** — Daily quote, quick stats, today's tip, quick action buttons
4. **Dashboard** — Track everything live: workouts, water, steps, schedule
5. **Explore** — Workouts · Diet · Steps · BMI · Progress · AI Coach · Settings
 
---
 
## 🏋️ Workout Split
 
| Day | Muscle Group | Exercises |
|-----|-------------|-----------|
| Monday | Chest | Bench Press, Incline DB Press, Cable Flyes + 5 more |
| Tuesday | Back | Deadlift, Pull-Ups, Barbell Row + 5 more |
| Wednesday | Legs | Squat, Romanian Deadlift, Leg Press + 5 more |
| Thursday | Shoulders | DB Press, Lateral Raises, Arnold Press + 5 more |
| Friday | Arms | Barbell Curl, Skull Crushers, Hammer Curls + 5 more |
| Saturday | Core & Cardio | Plank, Hanging Leg Raises, 20-min HIIT + 5 more |
| Sunday | 😴 Rest & Recovery | Recovery meals + stretching |
 
Complete **any 5 of 8** exercises per day. Each one logs the exact time you completed it.
 
---
 
## 🥗 Diet Plans
 
### Veg — Weekly Overview
 
| Day | Breakfast | Lunch | Dinner |
|-----|-----------|-------|--------|
| Mon | Power Oats Bowl | Paneer & Quinoa Bowl | Masoor Dal & Brown Rice |
| Tue | Tofu Scramble | Chickpea Salad Bowl | Palak Paneer & Roti |
| Wed | Greek Yogurt Parfait | Rajma Chawal | Moong Dal Khichdi |
| Thu | Semolina Upma & Egg | Soya Chunks Curry | Vegetable Biryani |
| Fri | Idli & Sambar | Chole Bhature | Moong Dal Soup & Rice |
| Sat | Protein Smoothie Bowl | Paneer Tikka Wrap | Mixed Dal Tadka |
| Sun | Turmeric Golden Milk Oats | Quinoa Roasted Veggie Bowl | Moong Dal Khichdi + Ghee |
 
### Non-Veg — Weekly Overview
 
| Day | Breakfast | Lunch | Dinner |
|-----|-----------|-------|--------|
| Mon | Scrambled Eggs & Toast | Grilled Chicken Rice Bowl | Baked Salmon & Quinoa |
| Tue | Chicken Omelette | Mutton Curry & Rice | Grilled Chicken & Sweet Potato |
| Wed | Tuna Avocado Toast | Chicken Biryani | Fish Curry & Rice |
| Thu | Egg Bhurji & Paratha | Prawn Stir Fry & Rice | Chicken Dal & Roti |
| Fri | High Protein Pancakes | Grilled Chicken Wrap | Egg Fried Rice |
| Sat | Mass Builder Shake | Chicken Pulao | Keema & Multigrain Roti |
| Sun | Salmon & Avocado Eggs | Turmeric Chicken & Sweet Potato | Baked Fish with Lemon & Herbs |
 
> **Sunday Recovery meals** are scientifically designed — anti-inflammatory ingredients, Omega-3 sources, and turmeric/ginger to speed up muscle repair.
 
---
 
## 🤖 AI Coach
 
The AI Coach is **fully built-in** — no API key, no internet required. It uses your actual profile data (weight, height, age, goal, activity level) to give personalised answers.
 
**Topics it covers:**
 
```
Protein targets          Pre/post workout meals    Chest exercises
Calorie needs (TDEE)     Rest days                 Back exercises
Muscle gain plan         Sleep & recovery          Leg exercises
Fat loss plan            HIIT vs Cardio            Shoulder exercises
BMI & body stats         Hydration needs           Arm exercises
Supplements guide        Step count tips           Core & abs
Motivation & mindset     Today's progress report   + more
```
 
---
 
## ⚖️ BMI Calculator
 
Supports **Metric** (kg / cm) and **Imperial** (lbs / ft + in).
 
| Metric Calculated | Formula Used |
|------------------|--------------|
| BMI | weight ÷ height² |
| Body Fat % | Deurenberg Formula (age + gender adjusted) |
| Ideal Body Weight | Devine Formula |
| Healthy Weight Range | BMI 18.5–24.9 for your height |
 
Outputs a visual animated gauge, sliding scale bar, colour-coded category badge, and a personalised action plan.
 
---
 
## 🔐 Auth & Security
 
| Feature | Detail |
|---------|--------|
| Sign Up | Name, email, password (min 8 chars) |
| Login | Email + password validation |
| Forgot Password | Enter email → set new password → auto-return to login |
| Session | Persisted in `localStorage` across browser sessions |
| Logout | Clears session, resets all state, redirects to landing page |
 
> ⚠️ **Note:** Passwords are stored as plain text in `localStorage`. This is a client-side demo app. Do not use real or sensitive passwords.
 
---
 
## 💾 Data & Privacy
 
- ✅ All data stored **locally** in your browser
- ✅ **No data is ever sent to any server**
- ✅ No analytics, no tracking, no cookies, no ads
- ✅ Works completely **offline** after first load
- ⚠️ Clearing your browser cache will erase saved accounts and progress
 
**localStorage keys used:**
 
| Key | Stores |
|-----|--------|
| `ax_users` | All registered accounts |
| `ax_sess` | Current logged-in session |
| `ax_today_{email}_{date}` | Daily progress (water, steps, exercises) |
 
---
 
## 🎯 Future Improvements
 
- 📱 PWA support — install as a mobile app
- ☁️ Cloud sync via Firebase or Supabase
- 📊 Advanced analytics — weekly and monthly trend graphs
- 🔔 Push notifications for workout and water reminders
- 🌍 Multi-language support
- 🖨️ Export progress as PDF report
- 🎵 Workout timer with audio cues
- 🤝 Social features — share progress with friends
 
---
 
## 📸 Screenshots
 
| Screen | Description |
|--------|-------------|
| Landing Page | Dark hero with gradient grid, feature cards, stats bar |
| Auth Page | Split panel — daily quote left, login/signup right |
| Home Page | Greeting + rotating quote + quick-stat cards + daily tip |
| Dashboard | Live stats + workout progress + hydration tracker |
| Workout View | Day tabs + exercise cards with complete/undo buttons |
| Diet Plans | Meal cards with macros + regenerate modal |
| BMI Calculator | Animated gauge + scale bar + advice panel |
| AI Coach | Chat interface + 8 quick prompt buttons |
| Settings | Profile edit + goal + password + daily targets |
 
*(Screenshots coming soon)*
 
---
 
## 👨‍💻 Author
 
**Parth**
GitHub: [@Parth-Tech-Creator](https://github.com/Parth-Tech-Creator)
 
---
 
## ⭐ Show Your Support
 
If you found RisePath helpful, give it a ⭐ on GitHub — it means a lot!
 
---
 
## 📄 License
 
This project is open source and available for personal use.
All fitness advice and meal plans are for general informational purposes only and do not constitute medical advice.
Always consult a qualified healthcare professional before starting any new diet or exercise programme.
 
---
 
*Built with ❤️ — RisePath. Rise every day. 🌅*
