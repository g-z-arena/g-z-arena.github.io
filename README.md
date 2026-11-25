<div align="center">

# 🎮 GZ Arena

### Your place to play, compete, and climb the leaderboard.

**GZ Arena** is an Arabic-first gaming hub that brings quick mini-games, friendly competition, player progression, and community events together in one responsive web experience.

[![Live Website](https://img.shields.io/badge/Live%20Demo-GZ%20Arena-2f7bff?style=for-the-badge&logo=googlechrome&logoColor=white)](https://g-z-arena.github.io/)
[![Hosted with GitHub Pages](https://img.shields.io/badge/Hosted%20on-GitHub%20Pages-181717?style=for-the-badge&logo=github)](https://pages.github.com/)
[![Firebase](https://img.shields.io/badge/Backend-Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)](https://firebase.google.com/)

</div>

---

## ✨ Overview

GZ Arena is a browser-based gaming platform designed around a simple idea: make casual gaming more social and rewarding. Players can create an account, try different challenges, earn experience points, unlock achievements, and compare their results on leaderboards.

The interface is built primarily for Arabic-speaking players, with right-to-left layout, a dark gaming-inspired visual theme, and responsive controls for mobile and desktop screens.

## 🚀 Features

### 🕹️ Games & Challenges
- **Snake** — classic arcade gameplay with keyboard, touch, and on-screen controls.
- **Reaction Test** — test your reflexes across multiple rounds.
- **Typing Challenge** — measure typing speed and accuracy.
- **Quiz Battles** — answer game-related questions and earn points.
- **Guess the Game** — identify games from emoji clues, with difficulty levels.
- **Social party games** — includes group-oriented game experiences such as Spy and Bomb Squad.

### 🏆 Player Progression
- Player accounts with email/password authentication.
- Customizable player names and avatars.
- XP rewards and level progression.
- Achievement badges for milestones and high scores.
- Personal statistics, including games played, wins, and best results.

### 📊 Competition & Community
- Leaderboards for XP, wins, quiz scores, and selected game records.
- Community events, tournaments, and challenges.
- Event registration and participant lists.
- Winner announcements for events.

### 🛠️ Admin Tools
- Admin dashboard for managing quiz questions and game puzzles.
- Create and publish tournaments, challenges, and events.
- View player rankings and award XP.
- Moderate supported community content.

### 📱 User Experience
- Arabic-first, right-to-left interface.
- Responsive layout for mobile and desktop.
- Dark visual theme with blue, purple, and gold accents.
- No frontend build step is required by the current project structure.

## 🧰 Tech Stack

| Technology | Role |
| --- | --- |
| HTML5 | Application structure |
| CSS3 | Responsive styling and visual design |
| Vanilla JavaScript (ES Modules) | Application logic and interactions |
| Firebase Authentication | Account registration and sign-in |
| Cloud Firestore | Player profiles, scores, questions, puzzles, and events |
| GitHub Pages | Static website hosting |
| Google Fonts | Arabic typography (Cairo and Changa) |

The current implementation loads Firebase Web SDK modules from Google's hosted CDN and does not use a Node.js package/build pipeline.

## 🌐 Live Demo

**Play GZ Arena:** https://g-z-arena.github.io/

## ⚙️ Local Setup

### 1. Clone the repository

```bash
git clone https://github.com/g-z-arena/g-z-arena.github.io.git
cd g-z-arena.github.io
```

### 2. Configure Firebase

The application currently keeps its Firebase web configuration and admin email near the beginning of the JavaScript module inside `index.html`.

1. Create a project in the [Firebase Console](https://console.firebase.google.com/).
2. Register a Web App in your Firebase project.
3. Enable **Authentication → Email/Password**.
4. Create a **Cloud Firestore** database.
5. Copy your Firebase web-app configuration into the `firebaseConfig` object in `index.html`.
6. Set the intended administrator email in `ADMIN_EMAIL`.
7. Add your deployment domain to Firebase Authentication's authorized domains.

> **Important:** The application references Firestore security rules during its setup guidance. Make sure you create and deploy appropriate Firestore rules before using a real deployment. Do not rely on frontend visibility or the `ADMIN_EMAIL` check as database authorization: enforce permissions, including administrator-only operations, in Firestore Security Rules.

### 3. Run locally

Because the app uses JavaScript ES modules, serve the folder through a local HTTP server rather than opening `index.html` directly.

For example, with Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

### 4. Deploy with GitHub Pages

1. Open the repository's **Settings → Pages**.
2. Choose **Deploy from a branch**.
3. Select the `main` branch and the `/ (root)` folder.
4. Save and wait for GitHub Pages to publish the site.

The site is served as a static frontend; Firebase provides authentication and cloud data services.

## 📁 Project Structure

```text
g-z-arena.github.io/
└── index.html       # Application markup, styles, and JavaScript
```

The current application is intentionally lightweight and self-contained in `index.html`.

## 🔐 Security Notes

- Firebase web configuration is intended to be included in client-side applications; it is not a substitute for database security.
- Configure Firestore Security Rules to restrict access to user data and validate all writes.
- Enforce administrator privileges in Firestore rules or trusted server-side logic. A client-side email comparison alone is not a security boundary.
- Never commit service-account credentials, private keys, or other server-side secrets to this public repository.

## 🗺️ Possible Future Improvements

- Add automated tests for game logic and important user flows.
- Move Firebase configuration to a clearly documented deployment configuration process.
- Separate the application into maintainable modules as the feature set grows.
- Add accessibility improvements and more detailed loading/error states.
- Add moderation and abuse-prevention safeguards for community features.

## 🤝 Contributing

Contributions, bug reports, and ideas are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Make your changes and test them locally.
4. Open a pull request with a clear description of the change.

For larger changes, consider opening an issue first to discuss the proposal.

## 📄 License

No license file was identified during this review. Unless a license is added to the repository, the project should not be assumed to be available for reuse, modification, or redistribution under an open-source license.

---

<div align="center">

**Built for players who love a little friendly competition.** 💙

[Visit GZ Arena](https://g-z-arena.github.io/) · [View Source Code](https://github.com/g-z-arena/g-z-arena.github.io)

</div>
