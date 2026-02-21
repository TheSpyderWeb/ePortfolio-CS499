# 🍳 Recipe Roulette

Recipe Roulette is a full-stack web application designed to make
discovering new recipes interactive, personalized, and engaging. Users
can generate random meals, search by ingredients, save favorites, and
interact with an AI-powered chatbot assistant called ChefBot.

------------------------------------------------------------------------

## 📌 Live Demo

\[ADD LIVE DEPLOYMENT LINK HERE\]

------------------------------------------------------------------------

## 📸 Screenshots

\[SCREENSHOT - HOMEPAGE\]

\[SCREENSHOT - SEARCH RESULTS\]

\[SCREENSHOT - FAVORITES PAGE\]

\[SCREENSHOT - CHEFBOT CHAT\]

------------------------------------------------------------------------

## 🚀 Features

### 🎲 Random Recipe Generator

-   Generates a new recipe every time the homepage loads
-   Uses MealDB API for dynamic recipe data

### 🔍 Search Recipes

-   Search by ingredient
-   Search by meal name
-   Dynamic rendering of search results

### ❤️ Favorites System

-   Save favorite recipes to Firestore
-   Retrieve user-specific saved meals
-   Persistent storage tied to authenticated users

### 🤖 ChefBot (AI Chat Assistant)

-   Provides recipe recommendations
-   Offers cooking tips
-   Shares fun food facts

### 🔐 User Authentication

-   Firebase Email/Password login
-   Secure user sessions
-   User-specific profile display

### 📱 Responsive Design

-   Optimized for desktop and mobile
-   Flexbox layout
-   Custom CSS styling
-   Lottie animations

------------------------------------------------------------------------

## 🛠️ Tech Stack

### Frontend

-   HTML5
-   CSS3
-   JavaScript (ES6+)
-   Lottie Animations

### Backend Services

-   Firebase Authentication
-   Firebase Firestore

### External API

-   MealDB API

------------------------------------------------------------------------

## 🧠 Software Engineering Concepts Demonstrated

-   Asynchronous JavaScript (fetch API, promises)
-   API integration
-   CRUD operations with Firestore
-   Authentication state management
-   DOM manipulation
-   Event-driven programming
-   Error handling and input validation
-   Responsive UI design principles

------------------------------------------------------------------------

## 🏗️ Project Architecture

-   Authentication logic separated from UI rendering
-   API calls modularized into reusable functions
-   Firestore collections structured by user ID
-   Event listeners handle dynamic user interactions

------------------------------------------------------------------------

## 💡 Technical Challenges & Solutions

### Handling Asynchronous Data

Used async/await and proper error handling to ensure the UI updates only
after API responses were received.

### Managing Authentication State

Implemented Firebase’s auth state listener to dynamically update UI
components when users log in or out.

### Firestore Data Structure

Structured collections to store favorites under unique user IDs to
ensure secure, personalized data access.

\[ADD MORE PERSONAL TECHNICAL CHALLENGES HERE\]

------------------------------------------------------------------------

## 🔮 Future Improvements

-   Add pagination for search results
-   Add filtering by cuisine or category
-   Implement recipe rating system
-   Improve chatbot intelligence
-   Add automated unit testing
-   Deploy fully using Firebase Hosting

------------------------------------------------------------------------

## 📂 Repository Structure

\[ADD FOLDER STRUCTURE OVERVIEW HERE\]

------------------------------------------------------------------------

## 🎓 Academic Context (CS499 Capstone)

This project was developed as part of the CS499 ePortfolio requirement.
It demonstrates cumulative knowledge in:

-   Full-stack development
-   Database integration
-   Secure authentication systems
-   API consumption
-   Responsive UI design
-   Software engineering best practices

------------------------------------------------------------------------

## 👩‍💻 Author

Reeham Imam  
Computer Science Student  
Southern New Hampshire University

GitHub: https://github.com/TheSpyderWeb

------------------------------------------------------------------------

## 📜 License

\[ADD LICENSE INFORMATION HERE\]
