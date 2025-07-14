# TeckFlow Project

This is a Next.js application built with Firebase Studio. It's designed to process, summarize, and store communications using AI.

## Getting Started

1.  **Install dependencies:**
    ```bash
    npm install
    ```

2.  **Set up environment variables:**
    Create a `.env` file in the root of the project and add your API keys:
    ```env
    # Your Google AI API Key for Genkit
    GOOGLE_API_KEY=YOUR_GEMINI_API_KEY
    
    # Your Firebase project configuration
    NEXT_PUBLIC_FIREBASE_API_KEY=YOUR_FIREBASE_API_KEY
    NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=YOUR_FIREBASE_AUTH_DOMAIN
    NEXT_PUBLIC_FIREBASE_PROJECT_ID=YOUR_FIREBASE_PROJECT_ID
    NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=YOUR_FIREBASE_STORAGE_BUCKET
    NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=YOUR_FIREBASE_MESSAGING_SENDER_ID
    NEXT_PUBLIC_FIREBASE_APP_ID=YOUR_FIREBASE_APP_ID
    NEXT_PUBLIC_FIREBASE_MEASUREMENT_ID=YOUR_FIREBASE_MEASUREMENT_ID
    ```

3.  **Run the development server:**
    ```bash
    npm run dev
    ```

Open [http://localhost:9002](http://localhost:9002) with your browser to see the result.

## Features

- **AI-Powered Summarization**: Upload documents (PDF, JPG, PNG) or paste text to get an AI-generated summary, key points, action items, and more.
- **Database Storage**: Each processed communication is saved as a record in Firebase Firestore.
- **Record Viewing**: A dedicated "Records" page displays all saved communications in a sortable, filterable table.
- **Data Export**: Export your records to CSV, XLSX, or SQL formats.
- **Date Filtering**: Filter records by a specific date or a date range.
- **Multi-language Support**: Switch between English and Spanish.
- **Responsive Design**: The application is designed to work on desktop, tablet, and mobile devices.
- **Light/Dark Mode**: Toggle between light and dark themes.

## Tech Stack

- **Framework**: Next.js (App Router)
- **AI**: Google Gemini via Genkit
- **Database**: Firebase Firestore
- **UI**: React, TypeScript, ShadCN UI, Tailwind CSS
- **Styling**: Tailwind CSS
- **Form Handling**: React Hook Form with Zod for validation
- **Internationalization (i18n)**: Custom context-based solution

## Firebase Setup

1.  Create a project on the [Firebase Console](https://console.firebase.google.com/).
2.  In your project, go to **Project settings** > **General**.
3.  Under "Your apps", click the web icon (`</>`) to add a new web app.
4.  Register your app and you will be provided with a `firebaseConfig` object. Copy these keys into your `.env` file as shown above.
5.  Go to **Firestore Database** in the left menu, create a database, and start in **test mode** for initial development (this allows open read/write access). For production, you will need to [secure your data with security rules](https://firebase.google.com/docs/firestore/security/get-started).
