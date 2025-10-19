hey , so i created this project ,while tackling the issue of unavailbility of resources for my endsem prep and for other exam prep .
this is the website that i have worked on which will return quizzes with vast amount of features.
just put in the data in backend/json file it will fetch the data and will present u with the best quiz.


# 📝 Quiz Mania — Interactive Quiz Web App

> A dynamic, interactive web application for taking quizzes online with real-time scoring and leaderboards

[![Node.js](https://img.shields.io/badge/Node.js-16+-green.svg)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-4.x-blue.svg)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-latest-brightgreen.svg)](https://www.mongodb.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 🎯 Overview

Quiz Master is a full-stack web application that supports fetching quiz questions from external APIs and custom JSON files. The platform features user authentication, real-time leaderboards, quiz timers, and a modern responsive UI.

---

## 🌟 Features

### Core Functionality
- 🔄 **Dynamic Question Sources**
  - Fetch questions from external APIs
  - Load custom questions from JSON files
  
- 🔐 **User Authentication**
  - Secure sign up and login system
  - User progress tracking with MongoDB
  - Session management

- 🎨 **Modern & Responsive UI**
  - Attractive design that works on all devices
  - Category-based quiz navigation
  - Intuitive user interface

- ⚡ **Instant Results**
  - Immediate scoring after completion
  - Real-time leaderboard updates
  - Performance analytics

- ⏱️ **Quiz Timer**
  - Countdown timer for each quiz
  - Automatic submission on timeout
  - Time pressure for added challenge

- 🏆 **Leaderboard System**
  - Top users displayed by score
  - Competitive ranking system
  - Encourages friendly competition

---
## 🖼️ Instances

### Home & Category Selection
![Home Page](https://github.com/Ayush2049/THE-ULTIMATE-QUIZ-WEB-APP/blob/0c02da5fb3597f620387463cd89c559dbd4149e7/project-instances/example1.png)

### Quiz in Progress with Timer
![Quiz Page](https://github.com/Ayush2049/THE-ULTIMATE-QUIZ-WEB-APP/blob/0c02da5fb3597f620387463cd89c559dbd4149e7/project-instances/example2.png)

### Results & Leaderboard
![Results Page](https://github.com/Ayush2049/THE-ULTIMATE-QUIZ-WEB-APP/blob/0c02da5fb3597f620387463cd89c559dbd4149e7/project-instances/example3.png)

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | HTML5, CSS3, JavaScript (ES6+) |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB |
| **APIs** | External Quiz API for dynamic content |

---

## 📂 Project Structure
```
quiz-app/
│
├── frontend/
│   ├── index.html              # Landing page
│   ├── quiz.html               # Quiz interface
│   ├── results.html            # Results page
│   ├── css/
│   │   └── style.css           # Styles
│   └── js/
│       ├── quiz.js             # Quiz logic
│       └── results.js          # Results handling
│
├── backend/
│   ├── app.js                  # Main server file
│   ├── routes/
│   │   ├── auth.js             # Authentication routes
│   │   ├── quiz.js             # Quiz routes
│   │   └── leaderboard.js      # Leaderboard routes
│   └── models/
│       ├── User.js             # User schema
│       └── Quiz.js             # Quiz schema
│
├── data/
│   └── customQuestions.json    # Custom quiz questions
│
├── .env                        # Environment variables
├── package.json                # Dependencies
└── README.md                   # Documentation
```

---

## 🚀 Installation & Setup

### Prerequisites

- Node.js 16+ installed
- MongoDB installed locally or MongoDB Atlas account
- Git

### Step-by-Step Guide

**1. Clone the repository**
```bash
git clone https://github.com/your-username/quiz-app.git
cd quiz-app
```

**2. Install dependencies**
```bash
npm install
```

**3. Configure Environment Variables**

Create a `.env` file in the root directory:
```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/quizmaster
SESSION_SECRET=your_secret_key_here
API_KEY=your_quiz_api_key
```

**4. Set up MongoDB**

- **Local Setup:** Ensure MongoDB is running on your machine
- **Cloud Setup:** Create a cluster on [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) and update `MONGODB_URI`

**5. Start the server**
```bash
node backend/app.js
```

Or use nodemon for development:
```bash
npm install -g nodemon
nodemon backend/app.js
```

**6. Access the application**

Open your browser and navigate to:
```
http://localhost:3000
```

---

## 📝 Usage Guide

### Getting Started

1. **Sign Up / Login**
   - Create a new account or login with existing credentials
   - Your progress and scores will be tracked

2. **Select a Quiz Category**
   - Browse available quiz categories
   - Choose based on your interest or difficulty level

3. **Take the Quiz**
   - Answer questions within the timer limit
   - Navigate between questions using Next/Previous buttons

4. **Submit & View Results**
   - Submit when finished or wait for auto-submission
   - See your score and correct answers immediately

5. **Check the Leaderboard**
   - View top performers
   - Track your ranking against other users

---

## 📊 Custom Questions Format

Add your own questions in `data/customQuestions.json`:
```json
[
  {
    "id": 1,
    "category": "JavaScript",
    "question": "What is the output of typeof null?",
    "options": [
      "null",
      "undefined",
      "object",
      "number"
    ],
    "correctAnswer": 2,
    "difficulty": "medium"
  },
  {
    "id": 2,
    "category": "JavaScript",
    "question": "Which method is used to parse a JSON string?",
    "options": [
      "JSON.parse()",
      "JSON.stringify()",
      "JSON.decode()",
      "JSON.read()"
    ],
    "correctAnswer": 0,
    "difficulty": "easy"
  }
]
```

---

## 🎨 Screenshots

### Landing Page
*[Add screenshot of your landing page]*

### Quiz Interface
*[Add screenshot of quiz in progress]*

### Results Page
*[Add screenshot of results display]*

### Leaderboard
*[Add screenshot of leaderboard]*

---

## 🔌 API Endpoints

### Authentication
- `POST /api/auth/signup` - Register new user
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout

### Quiz
- `GET /api/quiz/categories` - Get all categories
- `GET /api/quiz/:category` - Get questions by category
- `POST /api/quiz/submit` - Submit quiz answers

### Leaderboard
- `GET /api/leaderboard` - Get top users
- `GET /api/leaderboard/:userId` - Get user rank

---

## 🚀 Future Enhancements

- [ ] Social login integration (Google, Facebook, GitHub)
- [ ] Multiple question types (images, audio, video)
- [ ] Detailed user analytics dashboard
- [ ] Quiz creation interface for users
- [ ] Share results on social media
- [ ] Mobile app (React Native)
- [ ] Multiplayer live quiz mode
- [ ] AI-generated questions
- [ ] Certificate generation for quiz completion

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 🐛 Known Issues

- Timer may lag on slow network connections
- Leaderboard updates require page refresh (real-time socket integration planned)

---

## 👨‍💻 Author

**Ayush**

- 🐙 GitHub: [@your-username](https://github.com/your-username)
- 📧 Email: your.email@example.com
- 💼 LinkedIn: [Your Profile](https://linkedin.com/in/yourprofile)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Quiz API provider for dynamic questions
- MongoDB for database solutions
- Express.js community for excellent documentation
- All contributors and testers

---

## 🔗 Links

- **GitHub Repository:** [Quiz Master](https://github.com/your-username/quiz-app)
- **Live Demo:** [View Demo](https://your-demo-link.com) *(Optional)*
- **Documentation:** [Full Docs](https://your-docs-link.com) *(Optional)*

---

<div align="center">

**⭐ Star this repo if you find it helpful!**

**📝 Happy Quizzing!**

Made with ❤️ by Ayush

</div>
