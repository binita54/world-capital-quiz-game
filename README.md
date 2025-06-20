# 🌍 World Capital Quiz Game

A fun and interactive web-based quiz game to test your knowledge of world capitals! This project combines a backend powered by **Node.js**, **Express**, and **PostgreSQL** with frontend API integration to create an engaging user experience.

---

## 🚀 Features

- Multiple-choice quiz questions about world capitals  
- Dynamically fetches country and capital data using the **REST Countries API**  
- Stores user scores and game data in a **PostgreSQL** database  
- Backend handles game logic, scoring, and data persistence  
- Responsive and user-friendly interface  

---

## 🛠️ Tech Stack & Tools

- **Node.js** — JavaScript runtime environment  
- **Express.js** — Web framework for backend routing and APIs  
- **PostgreSQL** — Database to store user scores and game stats  
- **pg** — Node.js PostgreSQL client for database operations  
- **REST Countries API** ([https://restcountries.com/](https://restcountries.com/)) — External API for country and capital data  
- **HTML/CSS/JavaScript** — Frontend for quiz UI  
- **Nodemon** — Development tool for auto-restarting server  

---

## 📂 Project Structure

world-capital-quiz-game/
├── index.js # Main Express server with API routes and DB logic
├── public/ # Frontend files (HTML, CSS, client-side JS)
├── package.json # Node project metadata
├── db/ # SQL scripts or migration files 
├── views/ 
└── README.md


---

## ⚙️ Setup & Installation

### 1. Clone the repository

```bash
git clone https://github.com/binita54/world-capital-quiz-game.git
cd world-capital-quiz-game
```
## 2. Install dependencies
npm install

## 3. Setup PostgreSQL database
-Ensure PostgreSQL is installed and running locally
-Create a database (e.g., quiz_game_db)
-Create required tables, for example:
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  username VARCHAR(50) UNIQUE NOT NULL
);

CREATE TABLE scores (
  id SERIAL PRIMARY KEY,
  user_id INTEGER REFERENCES users(id),
  score INTEGER,
  played_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

## 4. Configure database connection
Edit the database configuration in index.js
const db = new Client({
  user: 'your_db_user',
  host: 'localhost',
  database: 'quiz_game_db',
  password: 'your_db_password',
  port: 5432,
});

## 5.Run the server
nodemon index.js
## 6. Open the app
http://localhost:3000

🔍 How It Works
-The frontend presents quiz questions about capitals of different countries.
-Questions and answers are populated dynamically using the REST Countries API.
-When a user finishes the quiz, their score and username are sent to the backend.
-Backend saves user info and scores in PostgreSQL for persistence.
-You can extend the app to add user authentication, leaderboards, and more!

   💡 Learning Outcomes
-Working with RESTful APIs (fetching live country data)
-Building backend API endpoints with Express
-Connecting Node.js with PostgreSQL for data storage
-Managing user sessions and score submissions
-Full-stack integration of frontend and backend


📄 License
This project is open-source and available under the MIT License.

🙋‍♀️ Author
👩 Binita
🔗 GitHub Profile
