Overview
This project is a simple yet fully functional web application for attempting quizzes, built as part of the FOSS Technical Team 2026 selection task. It uses the OpenTDB API to fetch trivia questions but proxies them through a custom backend to handle rate limits (1 request per 5 seconds) and make it "our own" by caching questions in memory. This avoids direct API calls from the frontend, improves performance, and prevents rate-limiting issues for multiple users.
The app focuses on IoT/tech-themed questions (from OpenTDB's "Computers" category). Users can start a quiz, answer multiple-choice questions, see correct/incorrect feedback, and get a final score.
Key considerations:

Direct use of OpenTDB isn't ideal for production due to rate limits and potential duplicates, so the backend caches a batch of questions on startup.
The UI is inspired by OpenTDB's style but customized with a colorful, neon dark theme for engagement.

This is 100% original work by Sachee.
Tech Stack

Frontend: HTML5, CSS3, Vanilla JavaScript (no frameworks for simplicity and performance).
Backend: Node.js with Express.js (for API routing), Axios (for API fetching), CORS (for cross-origin support).
API Integration: OpenTDB API (proxied and cached in backend).
Other: In-memory caching for questions; no external DB for minimal setup.
Deployment (Stretch): Frontend on Netlify, Backend on Render (free tiers). Docker for containerization (optional, see below).

Features

Responsive, colorful UI with a dark neon theme and IoT background.
Quiz flow: Start button, randomized options, instant feedback, score tracking.
Backend handles question fetching and caching to respect API limits.
Navigation bar with placeholders for future features (Browse, Add Questions, etc.).
Error handling for API failures.

