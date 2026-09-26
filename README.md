# CarbonCoach

> **See your meal. See its impact. Make the next choice.**

CarbonCoach is an AI-powered mobile application designed to make the environmental impact of food choices easier to understand.

The app allows users to identify a meal using an image, estimate its associated carbon footprint in **CO₂e**, and present the result in a simple, understandable way.

Instead of making sustainability an abstract concept, CarbonCoach connects it directly to something people interact with every day: **food.**

---

## ✨ What is CarbonCoach?

The environmental impact of a meal is often invisible to the person eating it.

CarbonCoach aims to make that impact visible.

The basic workflow is:

```
        📸 MEAL
           │
           ▼
    🤖 AI RECOGNITION
           │
           ▼
     🍽️ FOOD DATA
           │
           ▼
      🌍 CO₂e ESTIMATION
           │
           ▼
    💡 USER FEEDBACK
````

A user provides a meal image, CarbonCoach analyzes the meal, identifies the relevant food information, estimates its carbon footprint, and displays the result through the mobile interface.

---

# 🚀 Core Features

### 📸 AI Meal Recognition

Users can provide an image of their meal.

CarbonCoach uses AI-based meal detection to identify the food represented in the image.

The project includes support for:

* AI-based meal recognition
* Gemini-powered meal detection
* Custom-model meal detection

---

### 🌍 Carbon Footprint Estimation

After identifying the meal, CarbonCoach estimates its environmental impact and expresses the result as:

**CO₂e — carbon dioxide equivalent**

The result is presented in a user-friendly format rather than requiring users to interpret raw environmental datasets.

---

### 📊 Simple Environmental Feedback

CarbonCoach focuses on making the result understandable.

Instead of simply displaying a technical number, the application presents the estimated footprint as actionable information that can help users become more aware of the environmental consequences associated with food choices.

---

### 📱 Mobile-First Experience

CarbonCoach is built as a mobile application using **React Native and Expo**.

The interface is designed around a simple flow:

```
Identify Meal
     ↓
Analyze
     ↓
Calculate CO₂e
     ↓
Understand Impact
```

---

# 🧠 How CarbonCoach Works

## 1. User provides a meal

The user captures or provides an image representing their meal.

```
User
 │
 └──► Meal Image
```

---

## 2. The image is processed

The application processes the image and sends it through the meal-detection pipeline.

Depending on the implementation/configuration, CarbonCoach can use AI-based detection to interpret the meal.

```
Meal Image
     │
     ▼
Image Processing
     │
     ▼
Meal Detection
```

---

## 3. AI identifies the meal

The recognition layer determines the food/meal represented by the image.

CarbonCoach contains functionality for:

```text
                Meal Image
                     │
                     ▼
              ┌──────────────┐
              │ AI Detection │
              └──────────────┘
                 │        │
                 ▼        ▼
              Gemini   Custom Model
                 │        │
                 └────┬───┘
                      ▼
                Food Information
```

The application is structured so that the meal-recognition component can work with different detection approaches.

---

## 4. CO₂e is estimated

Once the relevant food information is available, CarbonCoach uses it to estimate the associated carbon footprint.

The output is represented as:

```
CO₂e
```

Carbon dioxide equivalent provides a common unit for expressing greenhouse-gas impact.

---

## 5. The result is presented to the user

The estimated footprint is returned to the mobile application and presented through the CarbonCoach interface.

The goal is to turn:

```
Raw environmental information
             ↓
        CO₂e estimate
             ↓
     Human-readable insight
```

---

# 🏗️ Technology Stack

| Technology                  | Purpose                             |
| --------------------------- | ----------------------------------- |
| **React Native**            | Mobile application framework        |
| **Expo**                    | Development and application runtime |
| **JavaScript / TypeScript** | Application logic                   |
| **Gemini**                  | AI-powered meal detection           |
| **Custom ML Model**         | Alternative meal detection pipeline |
| **Expo File System**        | Image/file handling                 |
| **Git / GitHub**            | Version control and collaboration   |

> The exact technologies and services may vary depending on the configured build and environment.

---

# 🧩 Application Architecture

At a high level, CarbonCoach follows this architecture:

```
┌──────────────────────┐
│        USER          │
└──────────┬───────────┘
           │
           │ Meal Image
           ▼
┌──────────────────────┐
│   React Native App   │
│        + Expo        │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│   Image Processing   │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│    Meal Detection    │
│                      │
│ Gemini / Custom ML   │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│    Food Information  │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│   CO₂e Estimation    │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│   CarbonCoach UI     │
│                      │
│  Environmental      │
│      Feedback        │
└──────────────────────┘
```

---

# 🎯 Why CarbonCoach?

Food choices are made every day, but their environmental impact is not always visible at the point of decision.

CarbonCoach explores a simple idea:

> **If environmental impact becomes visible, it becomes easier to understand.**

By connecting food recognition with carbon-footprint estimation, CarbonCoach aims to put sustainability information directly into the user's everyday decision-making process.

---

# 🛠️ Getting Started

## Prerequisites

Make sure you have the following installed:

* [Node.js](https://nodejs.org/)
* npm
* Expo CLI / Expo tooling
* Git
* Expo Go (for testing on a physical mobile device)

---

## Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/CarbonCoach.git
```

Navigate into the project:

```bash
cd CarbonCoach
```

---

## Install Dependencies

```bash
npm install
```

If you are using PowerShell on Windows and encounter an execution-policy error with `npm`, you can use:

```powershell
npm.cmd install
```

---

## Start the Development Server

```bash
npx expo start
```

On Windows PowerShell, if `npx` is blocked by the execution policy:

```powershell
npx.cmd expo start
```

Expo will start the development server and display options for running the application.

---

## Run on a Physical Device

1. Install **Expo Go** on your Android/iOS device.
2. Connect your computer and phone to the appropriate network.
3. Start the Expo development server:

```bash
npx expo start
```

4. Scan the displayed QR code using Expo Go.

---

## Run on Web

If web support is configured in the project:

```bash
npm run web
```

or:

```bash
npm.cmd run web
```

---

# 🔐 Environment Variables

If the application requires API keys or external services, configure them through environment variables rather than committing credentials to GitHub.

For example:

```env
EXPO_PUBLIC_GEMINI_API_KEY=your_api_key_here
```

**Never commit real API keys, tokens, passwords, or other secrets to the repository.**

Add sensitive environment files such as:

```
.env
.env.local
```

to `.gitignore`.

---

# 📁 Project Structure

A typical CarbonCoach structure looks like:

```
CarbonCoach/
│
├── assets/
│   ├── images/
│   └── ...
│
├── components/
│   └── ...
│
├── screens/
│   └── ...
│
├── services/
│   ├── mealDetection/
│   └── ...
│
├── utils/
│   └── ...
│
├── App.js / App.tsx
├── package.json
├── app.json
├── .gitignore
└── README.md
```

The exact structure may differ depending on the current implementation.

---

# ⚠️ Current Limitations

CarbonCoach is a hackathon project and should be considered a prototype.

Potential sources of uncertainty include:

* Meal recognition accuracy can vary depending on image quality and meal complexity.
* Carbon-footprint estimates depend on the underlying food/environmental data.
* Mixed meals can be more difficult to identify accurately.
* Results should be treated as estimates rather than precise measurements.
* Some AI functionality may require an internet connection and configured API credentials.

CarbonCoach does **not** claim that its estimates represent the exact environmental footprint of every individual meal.

---

# 🔮 Future Development

Potential future improvements include:

* More comprehensive food/carbon datasets
* Improved recognition of mixed meals
* Regional food and production data
* Personalized sustainability insights
* Meal history and footprint tracking
* Food-choice comparisons
* Improved offline capabilities
* More detailed environmental-impact visualization
* Integration with additional AI/ML models

---

# 🌱 Vision

CarbonCoach is built around a simple vision:

### Make the invisible visible.

Food is something everyone interacts with.

By connecting everyday meals with understandable environmental information, CarbonCoach explores a more accessible approach to sustainability awareness.

```
              FOOD
                │
                ▼
          AI RECOGNITION
                │
                ▼
             CO₂e
                │
                ▼
          UNDERSTANDING
                │
                ▼
        INFORMED CHOICES
```

---

# 👥 Team

**CarbonCoach — Hackathon Project**

Built with:

* React Native
* Expo
* AI-powered meal recognition
* Carbon-footprint estimation

---
