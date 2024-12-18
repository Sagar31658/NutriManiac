# AI-Powered Fitness & Nutrition Recommendation System

This repository hosts a comprehensive platform that leverages machine learning to guide users toward their fitness and nutrition goals. By understanding each user's profile, dietary constraints, workout preferences, and personal objectives, the system provides tailored calorie recommendations, exercise routines, and meal plans. Additionally, it supports progress tracking and enhances user motivation through regular tips, quotes, and podcast suggestions.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [System Flow](#system-flow)
- [Data Inputs](#data-inputs)
- [Machine Learning Components](#machine-learning-components)
- [User Interaction](#user-interaction)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Configuration](#configuration)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Overview
This solution integrates a frontend (React) for user interaction, a backend (Node.js) for business logic and API services, and a ML service (Python/FastAPI) for generating personalized recommendations. Users specify their fitness goals (bulk, cut, maintain), exercise environment (home/gym), and dietary restrictions (Veg/Non-Veg/Egg/Allergies). The system then suggests a daily calorie target, a corresponding workout schedule, and balanced meal plans. It also allows users to modify recommendations, track their progress over time, and receive motivational content at their chosen frequency.

## Features
- **User Profile & Goals**: Collects name, age, height, weight, workout experience, target goal, and preferred exercise setting.
- **Dietary Restrictions**: Customizes meal plans based on vegetarian, non-vegetarian, egg-based preferences, and specific allergies.
- **Calorie Recommendation**: Provides an ML-driven baseline calorie target (surplus/deficit/maintenance), adjustable by the user.
- **Workout Plan Generation**: Translates the calorie target and user’s workout schedule into a structured exercise plan, supplemented with instructional videos.
- **Meal Recommendations**: Suggests meals (breakfast, lunch, dinner) aligned with the user’s calorie and dietary needs, including nutrient breakdowns.
- **Meal Editing & Nutrition Updates**: Users can replace recommended meals with their own ingredients and get immediate nutritional recalculations.
- **Progress Tracking**: Logs user adherence, dietary changes, and workout consistency, refining future recommendations.
- **Motivational Content Delivery**: Sends curated quotes, tips, and podcast suggestions at user-defined intervals to maintain engagement.

## System Flow
1. **User Onboarding**: User registers and provides personal data and fitness objectives.
2. **Calorie Calculation**: ML model suggests a daily calorie target, which the user can adjust.
3. **Workout Scheduling**: Based on the finalized calorie intake and workout frequency/environment, the system recommends a tailored exercise routine.
4. **Meal Planning**: The ML model generates daily meal suggestions that respect calorie goals and dietary restrictions.
5. **User Interaction & Customization**: Users accept or tweak recommendations, adding custom ingredients for up-to-date nutrition info.
6. **Progress Logging**: The system monitors user data over time, adapting recommendations as goals and habits evolve.
7. **Motivation & Engagement**: Regular motivational content is delivered, reinforcing healthy behaviors.

## Data Inputs
- **User Attributes**: Name, age, height, weight, and fitness experience level.
- **Goals & Preferences**: Desired outcome (bulk/cut/maintain), days available for exercise, and chosen setting (home/gym).
- **Dietary Constraints**: Vegetarian, non-vegetarian, egg-based diets, or any allergies.
- **User Feedback**: Adjusted calorie targets, chosen meals, logged ingredients, and adherence patterns.

## Machine Learning Components
- **Calorie Estimator**: Determines maintenance, surplus, or deficit calorie targets.
- **Workout Recommender**: Generates exercise schedules based on user’s goals, calorie targets, and environment.
- **Meal Planner**: Creates meal recommendations tailored to dietary restrictions and nutrition goals.
- **Adaptive Learning**: Continuously refines suggestions using user progress and adherence data.

## User Interaction
- **Frontend (React)**:  
  - Registration/Login  
  - Profile dashboard (calories, workouts, meals)  
  - Meal input & editing  
  - Progress visualization  
  - Notification frequency settings
- **Backend (Node.js)**:
  - Manages user profiles, sessions, and requests  
  - Interfaces with ML services for real-time recommendation updates
- **ML Service (Python/FastAPI)**:
  - Provides calorie, workout, and meal predictions  
  - Iteratively updates models as new user data arrives

## Project Structure
my-project/ 
        ├─frontend/ # React SPA for user interface 
        ├─ backend/ # Node.js server for APIs & business logic 
        └─ ml/ # Python/FastAPI ML models & inference endpoints

## Getting Started  **Install Dependencies for Each Part:**  -          **Frontend**:
    cd frontend
    npm install

**Backend**
    cd backend
    npm install
    
**ml**
    pip install -r requirements.txt
    

*   **Run Each Service:**

    **frontend**
    npm start
    Access at [http://localhost:3000](http://localhost:3000)
    **backend**
    cd backend
    npm run start
    **ML**    
    cd ml
    uvicorn app.main:app --reload
    

Configuration
-------------

Use environment variables to set secrets, API keys, and database credentials. Configure .env files or use a secrets manager (e.g., AWS Secrets Manager) for secure storage.

Usage
-----

1.  Open the frontend at [http://localhost:3000](http://localhost:3000).
    
2.  Sign up and configure your profile (goals, dietary restrictions, etc.).
    
3.  Explore the personalized calorie recommendations, workout plans, and meal suggestions.
    
4.  Adjust calorie targets or replace meals with your own ingredients to see updated nutritional data in real time.
    
5.  Track your progress over time and receive motivational content as per your chosen frequency.
    

Contributing
------------

*   **Branching Model**: Use feature branches off develop and submit pull requests for code reviews.
    
*   **Testing**: Add unit and integration tests for each service and run them before submitting PRs.
    
*   **Code Style**: Follow ESLint and Prettier conventions for the frontend and PEP 8 for Python code in the ML service.
    

License
-------

This project is licensed under the MIT License.