# 📲 MyTrackr

**MyTrackr** is a mobile-first Android app that helps users effortlessly scan, store, and track receipts while managing monthly budgets. The app leverages **ML Kit Text Recognition** and **Gemini API** to extract and structure receipt data into a consistent JSON format for easy expense tracking, visualization, and financial insights.

## 🎥 Demo Video

Watch the app in action: [MyTrackr Demo Video](https://drive.google.com/file/d/1tHRllKTm7k0Ls3zdUt1d1hlyeeQKWHEm/view?usp=sharing)

## 📥 Download APK

Download and install the app: [MyTrackr APK](https://drive.google.com/file/d/1kYrE3AWDOlBrphaHAGSRLBk6wS_suy9B/view?usp=sharing)

---

## 🚀 Features

### 🛬 Onboarding

- Interactive onboarding pages with ViewPager2 explaining:
  - App functionality and benefits
  - Digital receipt management advantages
  - Budget tracking capabilities

### 🔐 Authentication & Access

- User Registration & Login (Email/Password)
- **Google Sign-On (SSO)** integration via Firebase Authentication
- Profile management with customizable settings

### 📸 Receipt Scanning & Processing

- Capture receipt images via **Camera** or select from **Gallery**
- Image preprocessing (scaling, whitespace trimming, contrast enhancement)
- **ML Kit Text Recognition** for OCR text extraction
- **Gemini API integration** to parse extracted text into structured JSON:
  - Store name and location
  - Transaction date and time
  - Itemized purchases with prices
  - Taxes and total amount
  - Payment method and category

### 💾 Expense Management

- **Chronological expense tracking** – transactions are categorized by purchase date, not scan date
- **Manual expense entry** for transactions without receipts
- Month-based expense organization and filtering
- Receipt and expense history with detailed breakdowns
- Category-based transaction grouping (Groceries, Meal, Entertainment, Travel, Shopping, Tax, Other)

### 💰 Budget Tracker

- Set and edit **monthly budgets**
- Real-time spending calculations synced with receipts and manual expenses
- **Daily notifications** for budget tracking using WorkManager and AlarmManager
- Progress indicators showing spent vs. remaining budget
- Receipt count and manual transaction count tracking

### 📊 Analytics Dashboard

- **Interactive data visualizations** using MPAndroidChart:
  - **Pie charts** for category-based spending distribution
  - **Bar charts** for time-series expense comparisons
  - **Line charts** for spending trend analysis
- Multiple time range filters:
  - Daily, Weekly, Monthly, Yearly, Custom range
- Category-specific drill-down with detailed transaction lists
- Real-time synchronization with Firebase data

### 👤 User Profile & Settings

- Customizable user profile with photo upload
- **Multi-language support** (English, French, Hindi, Chinese)
- **Theme switching** (Light/Dark mode)
- Profile information management

### 🔔 Notifications

- Daily budget reminder notifications
- Scheduled notifications using Android WorkManager
- Calendar-based notification calculations

---

## 🏗️ Tech Stack

- **Frontend (Mobile):** Android (Java)
- **Authentication:** Firebase Auth (Email/Password + Google SSO)
- **OCR:** Google ML Kit Text Recognition API
- **AI Processing:** Google Gemini 2.5 Flash API (structured data extraction)
- **Database:** Firebase Firestore (transaction data, budgets, user profiles)
- **Storage:** Firebase Storage (receipt images), Cloudinary (image optimization)
- **Data Visualization:** MPAndroidChart (pie, bar, line charts)
- **Build System:** Gradle (Kotlin DSL)
