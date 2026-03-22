# RisePath — Fitness Tracker

> Your complete fitness operating system. Smart workouts, personalised nutrition, real-time step tracking, BMI calculator, and a built-in AI coach — all in a single HTML file.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Getting Started](#getting-started)
- [Pages & Sections](#pages--sections)
- [AI Coach](#ai-coach)
- [Diet Plans](#diet-plans)
- [BMI Calculator](#bmi-calculator)
- [Step Counter](#step-counter)
- [Settings & Customisation](#settings--customisation)
- [Forgot Password](#forgot-password)
- [Tech Stack](#tech-stack)
- [Data & Privacy](#data--privacy)
- [File Structure](#file-structure)
- [Screenshots Overview](#screenshots-overview)
- [Known Limitations](#known-limitations)

---

## Overview

**RisePath** is a fully self-contained, single-file fitness tracker built with plain HTML, CSS, and JavaScript. No installation, no backend, no database, no internet required (except for web fonts). Just open `RisePath.html` in any modern browser and start tracking.

Everything — user accounts, workout progress, water intake, step count, diet preferences, settings — is stored in your browser's `localStorage` so your data persists between sessions.

---

## Features

| Feature | Details |
|---|---|
| 🔐 Auth System | Sign up / Login / Forgot Password — stored in localStorage |
| 🏋️ Workout Plans | 6-day muscle split, 8 exercises/day, complete any 5 |
| 🥗 Diet Plans | Veg & Non-Veg, Mon–Sun (including Sunday Recovery), Regenerate with preferences |
| 👣 Step Counter | Real accelerometer sensor on mobile, manual buttons on desktop |
| 💧 Hydration Tracker | Log glasses with timestamps, 45-min reminders |
| 📊 Dashboard | Live stats — exercises, water, steps, active days |
| ⚖️ BMI Calculator | Metric & Imperial, body fat %, ideal weight, personalised advice |
| 🤖 AI Coach | Built-in offline coach — calculates protein, calories, BMI, and more |
| 📈 Progress | 8-week weight trend, achievements, today's live report |
| ⚙️ Settings | Update profile, goal, activity, password, daily targets |
| 🌙 Daily Quotes | 31 rotating motivational quotes (changes by day of year) |
| 🔑 Forgot Password | Reset password via email verification against stored account |

---

## Getting Started

### Run Locally

1. Download `RisePath.html`
2. Open it in any modern browser (Chrome, Firefox, Safari, Edge)
3. No server required — double-click to open

### First Time Setup

1. **Landing page** → Click **"Start For Free"**
2. **Sign Up** → Enter your name, email, and a password (min 8 characters)
3. **Profile Setup** (3 steps):
   - Step 1: Height, Weight, Age, Gender
   - Step 2: Activity Level (Sedentary → Extremely Active)
   - Step 3: Fitness Goal (Lose Weight / Gain Muscle / Maintain / Endurance / Strength)
4. You're in! The app loads your personalised dashboard

### Returning Users

Open the file → Click **"I Already Have an Account"** → Enter email and password → Dashboard loads with all your saved progress.

---

## Pages & Sections

### Landing Page
- Hero headline with animated background grid
- Feature overview (6 cards)
- "How RisePath works" 3-step explainer
- Stats bar (muscle groups, exercises, AI, daily quotes)
- Bottom CTA

### Auth Page
- **Left panel**: Today's daily quote + list of platform features
- **Right panel**: Login / Sign Up tabs
- Forgot password flow built in

### Profile Setup
- 3-step wizard (Basic Info → Activity Level → Fitness Goal)
- Progress indicators at the top
- Returning users skip setup if profile is already complete

### Home Page (after login)
- Personalised greeting (Good morning/afternoon/evening)
- Daily motivational quote (rotates every day)
- 4 quick-stat cards: Exercises, Water, Steps, Days Active
- Quick action buttons (Start Workout, View Diet, Track Steps, Ask AI)
- Today's fitness tip (7 rotating science-based tips)
- "Your plan at a glance" 3 cards
- Floating AI Coach button (bottom-right)

### Dashboard
- 4 stat boxes (live): Exercises Done, Water, Steps, Days Active
- Today's Workout Progress bar list
- Hydration Tracker with glass icons + timestamped log
- Step Progress (goal %, calories burned, distance)
- Today's Schedule (4 checkable items)

### Workouts
- 6 workout days (Mon–Sat) + Sunday Rest
- 8 exercises per day, complete **any 5**
- Each exercise: name, description, sets/reps, Watch Tutorial link, ✓ Complete button
- Completed exercises show timestamp and green highlight
- Day progress bar fills to 100% at 5/5
- Today's day auto-highlighted with ★

**Workout Split:**
| Day | Muscle Group |
|-----|-------------|
| Monday | Chest |
| Tuesday | Back |
| Wednesday | Legs |
| Thursday | Shoulders |
| Friday | Arms |
| Saturday | Core & Cardio |
| Sunday | Rest & Recovery |

### Diet Plans
- Veg / Non-Veg toggle
- Full 7-day plan (Mon–Sun) including Sunday Recovery meals
- Each meal: name, 5 food components, macros (P/C/F)
- Daily totals bar: Calories, Protein, Carbs, Fats
- **Regenerate** button with full preference modal
- "Not loving this plan?" bar at the bottom

### Step Counter
- Real `DeviceMotionEvent` accelerometer on mobile (peak-detection algorithm)
- SVG ring progress indicator
- Start/Pause toggle
- Manual +100 / +500 / +1K / −100 buttons (for desktop)
- Week overview bar chart
- 10,000 step goal notification

### Progress
- 8-week weight trend bar chart
- Today's Live Report (exercises, water, steps, calories burned, distance)
- 6 achievements that unlock based on real actions

### AI Coach
- Fully built-in, works offline, no API key needed
- Personalised responses using your profile (weight, height, age, goal, activity)
- Covers: protein targets, calorie needs, BMI, pre/post workout meals, rest days, sleep, HIIT, all muscle groups, hydration, supplements, motivation, and more
- 8 quick prompt buttons on the side
- Typing animation before each reply
- Floating FAB button from home page

### BMI Calculator
- **Metric** (kg / cm) and **Imperial** (lbs / ft + in) modes
- "Use my profile data" button auto-fills from saved profile
- Animated gauge with colour-coded needle
- Sliding scale bar with category marker
- Stats calculated: BMI, body fat % (Deurenberg), ideal body weight (Devine), kg to lose/gain
- Personalised advice panel per category
- Healthy weight range for your height
- Full WHO classification table (6 categories)

### Settings
- Update name, height, weight, age, gender
- Change fitness goal (5 options)
- Change activity level (5 options)
- Change password (requires current password)
- Customise daily step goal and water goal
- Switch diet preference (Veg / Non-Veg)
- Export data as JSON
- Reset today's progress
- Sign Out

---

## AI Coach

The AI Coach is a built-in rule-based engine — no internet or API key required.

### What it can answer

| Topic | Example question |
|---|---|
| Protein | "How much protein do I need?" |
| Calories | "How many calories should I eat?" |
| Muscle gain | "How do I build muscle?" |
| Fat loss | "How do I lose weight?" |
| Pre-workout | "What should I eat before a workout?" |
| Post-workout | "What should I eat after training?" |
| Rest days | "How many rest days do I need?" |
| Sleep | "How does sleep affect muscle growth?" |
| HIIT / Cardio | "Is HIIT better than steady cardio?" |
| Chest | "Best chest exercises?" |
| Back | "How do I build a wide back?" |
| Legs | "Best leg exercises?" |
| Shoulders | "How do I get wider shoulders?" |
| Arms | "How do I get bigger arms?" |
| Core | "How do I get visible abs?" |
| Hydration | "How much water should I drink?" |
| Steps | "How do I hit 10,000 steps?" |
| BMI | "What is my BMI?" |
| Supplements | "Should I take creatine?" |
| Motivation | "I feel like giving up" |
| Progress | "Show me my progress today" |

All answers use your actual profile data (weight, height, age, goal, activity level) for personalised numbers.

---

## Diet Plans

### Weekly Structure (Veg)

| Day | Breakfast | Lunch | Dinner |
|-----|-----------|-------|--------|
| Monday | Power Oats Bowl | Paneer & Quinoa Bowl | Masoor Dal & Brown Rice |
| Tuesday | Tofu Scramble | Chickpea Salad Bowl | Palak Paneer & Roti |
| Wednesday | Greek Yogurt Parfait | Rajma Chawal | Moong Dal Khichdi |
| Thursday | Semolina Upma & Egg | Soya Chunks Curry & Roti | Vegetable Biryani |
| Friday | Idli & Sambar | Chole Bhature | Moong Dal Soup & Rice |
| Saturday | Protein Smoothie Bowl | Paneer Tikka Wrap | Mixed Dal Tadka & Roti |
| Sunday | Turmeric Golden Milk Oats | Quinoa & Roasted Veggie Bowl | Moong Dal Khichdi with Ghee |

### Weekly Structure (Non-Veg)

| Day | Breakfast | Lunch | Dinner |
|-----|-----------|-------|--------|
| Monday | Scrambled Eggs & Toast | Grilled Chicken Rice Bowl | Baked Salmon & Quinoa |
| Tuesday | Chicken Omelette | Mutton Curry & Rice | Grilled Chicken & Sweet Potato |
| Wednesday | Tuna Avocado Toast | Chicken Biryani | Fish Curry & Rice |
| Thursday | Egg Bhurji & Paratha | Prawn Stir Fry & Rice | Chicken Dal & Roti |
| Friday | High Protein Pancakes | Grilled Chicken Wrap | Egg Fried Rice |
| Saturday | Mass Builder Shake | Chicken Pulao | Keema & Multigrain Roti |
| Sunday | Salmon & Avocado Eggs | Turmeric Chicken & Sweet Potato | Baked Fish with Lemon & Herbs |

### Sunday Recovery Meals
Sunday is specifically designed for **muscle recovery** — anti-inflammatory ingredients, Omega-3 sources, and easily digestible proteins. Each meal includes a 💡 recovery tip explaining the science.

### Regenerate Plan
Click **"Regenerate Plan"** to customise meals by:
- Cuisine style (Indian, Mediterranean, Asian, Middle Eastern, Clean)
- Calorie target (Low / Moderate / High / Bulk)
- Meal focus (High Protein / Whole Foods / Low Carb / Carb Heavy / Quick & Easy)
- Foods to avoid (Dairy, Gluten, Nuts, Seafood, Spicy, Onion/Garlic)
- Which day to regenerate (All Days or specific day)

---

## BMI Calculator

### Formulas Used

| Metric | Formula |
|--------|---------|
| BMI | weight(kg) ÷ height(m)² |
| Body Fat % | (1.2 × BMI) + (0.23 × age) − (10.8 × sex) − 5.4 — Deurenberg |
| Ideal Body Weight | 50 + 2.3 × (height_inches − 60) for men / 45.5 for women — Devine |

### BMI Categories (WHO)

| Category | BMI Range |
|----------|-----------|
| Underweight | < 18.5 |
| Normal weight | 18.5 – 24.9 |
| Overweight | 25 – 29.9 |
| Obese Class I | 30 – 34.9 |
| Obese Class II | 35 – 39.9 |
| Obese Class III | ≥ 40 |

---

## Step Counter

On **mobile devices** with motion sensors, the step counter uses the `DeviceMotionEvent` API with a peak-detection algorithm:

- Reads `accelerationIncludingGravity` (x/y/z axes)
- Applies a low-pass filter (α = 0.8) to smooth noise
- Detects steps as acceleration peaks > 1.2g above gravity baseline
- Enforces 250ms minimum gap between steps to prevent double-counting
- iOS 13+ requires explicit permission prompt

On **desktop** (no sensor), use the manual **+100 / +500 / +1K / −100** buttons.

---

## Settings & Customisation

### Profile Fields
- Full Name, Email (read-only), Height (cm), Weight (kg), Age, Gender

### Daily Targets
- Step goal (default: 10,000, range: 1,000–50,000)
- Water goal (default: 8 glasses, range: 4–20)
- Diet preference (Veg / Non-Veg)

### Password Change
Requires current password. New password must be 8+ characters.

### Data Export
Downloads a `.json` file containing your full profile and today's progress data.

---

## Forgot Password

1. On the Login page, click **"Forgot password?"** next to the Password field
2. Enter your registered email
3. Enter and confirm a new password (min 8 characters)
4. Click **"Reset Password"**
5. On success, the form auto-returns to login after 2 seconds with your email pre-filled

**Note:** If you had already typed your email in the login field before clicking "Forgot password?", it will be pre-filled in the reset form automatically.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Structure | HTML5 |
| Styling | CSS3 (custom properties, grid, flexbox, animations) |
| Logic | Vanilla JavaScript (ES6+) |
| Fonts | Google Fonts — Inter, Bebas Neue, Space Mono |
| Storage | Browser `localStorage` (no server, no database) |
| Motion API | `DeviceMotionEvent` (step tracking on mobile) |
| No frameworks | No React, Vue, Angular, jQuery |
| No build tools | No webpack, vite, npm — just open the file |

---

## Data & Privacy

- **All data is stored locally** in your browser's `localStorage`
- No data is ever sent to any server
- No analytics, no tracking, no cookies
- No ads — RisePath is completely ad-free
- Clearing browser data / cache will erase your stored accounts and progress
- The file is fully self-contained — you can use it offline after the initial load (web fonts require internet on first load)

### What is stored in localStorage

| Key | Contents |
|-----|----------|
| `ax_users` | All user accounts (name, email, hashed\* password, profile) |
| `ax_sess` | Current session (logged-in user data) |
| `ax_today_{email}_{date}` | Daily progress (water, steps, exercises, schedule) |

> \* Note: Passwords are stored as plain text in localStorage. This is a client-side demo app — do not use real/important passwords.

---

## File Structure

```
RisePath.html          ← The entire app (single file, ~590 KB)
README.md              ← This file
```

The HTML file contains:
- All CSS (embedded in `<style>` tags)
- All JavaScript (embedded in `<script>` tags)
- The RisePath logo (embedded as base64 PNG)
- All meal data, workout data, quote arrays, and tip content inline

---

## Screenshots Overview

| Screen | Description |
|--------|-------------|
| Landing | Dark hero with gradient grid, feature cards, how-it-works section |
| Auth | Split panel — daily quote on left, login/signup on right |
| Profile Setup | 3-step wizard with progress dots |
| Home | Greeting + quote + quick stats + daily tip |
| Dashboard | 4 stat boxes + workout progress + water tracker + step bars |
| Workouts | Day tabs + exercise cards with complete/undo buttons |
| Diet | Meal cards with macros + regenerate modal |
| Steps | SVG ring + week bar chart + manual buttons |
| BMI | Gauge + scale bar + stats grid + advice panel |
| Progress | Weight trend + achievements + live report |
| AI Coach | Chat interface + quick prompts sidebar |
| Settings | 5 cards — profile, goal/activity, password, targets, data |

---

## Known Limitations

| Limitation | Details |
|-----------|---------|
| Single browser | Data is tied to the browser and device it was created on |
| Plain text passwords | localStorage is not encrypted — do not use real passwords |
| No cloud sync | Progress does not sync across devices |
| Step sensor | Requires a physical device with accelerometer (not available in most desktop browsers) |
| Font dependency | Google Fonts requires internet connection on first load |
| BMI accuracy | BMI and body fat estimates are screening tools, not medical diagnostics |
| AI Coach | Built-in rule-based engine — not a real language model; complex queries default to general advice |

---

## Version History

| Version | Changes |
|---------|---------|
| 1.0 | Initial release — auth, workouts, diet, steps, dashboard |
| 1.1 | Settings page, profile editing, password change |
| 1.2 | AI Coach (built-in), BMI Calculator |
| 1.3 | Sunday recovery diet, Regenerate plan modal, meal improvements |
| 1.4 | RisePath branding, custom logo, forgot password, README |

---

## License

This project is for personal use. All meal plans, workout data, and fitness advice are for general informational purposes only and do not constitute medical advice. Always consult a qualified healthcare professional before starting any new diet or exercise programme.

---

*Built with ❤️ — RisePath. Rise every day.*
