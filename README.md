# LearnLoop - Premium Skill Barter Platform (Frontend Demo)

LearnLoop is a community-driven skill exchange platform where users teach what they know and learn what they want through a skill barter system. This is a fully client-side implementation featuring futuristic aesthetics, animations, glassmorphism, responsive dashboards, and interactive database simulations driven by browser `localStorage`.

---

## ✨ Premium Features Included

1. **Futuristic UX/UI Design**: Complete Dark Mode (primary) and Light Mode customization, premium Outfit typography, backdrop blurs, glow effects, floating elements, custom glowing cursor tracking, scroll progress bar, and smooth transitions.
2. **LinkedIn-Style Professional Profile**: Rebuilt to resemble a professional dashboard showing:
   - Header Card with Avatar overlapping cover picture.
   - Professional Headline, Location, and connection stats.
   - **Community Activity Feed (Photo Sharing)**: Share study moments, workspace snapshots, whiteboard ideas, and gold certificates with custom SVG vector illustrations and interactive post likes counters.
   - **Exchange Experience Section**: Displays Completed Sessions formatted like professional experience logs.
   - **Skills with Endorsements**: Endorsements count labels on skills offered/wanted chips.
3. **Interactive Dashboard**: Dynamically calculated metrics (Skills Offered, Skills Wanted, Active Requests, Completed Hours, Average Rating), custom interactive SVG Line charts (Learning vs Teaching Activity), calendar schedule agenda highlights, messaging snippets, and badges shelf.
4. **Smart Skill Matching**: Dynamic compatibility score (calculated on mutual skill barter matching of wanted vs offered lists), search query filters, level selects, and availability selectors.
5. **Active Request Lifecycle**: Incoming proposals tab (Accept / Reject), Outgoing proposals (Cancel), and historical lists with status badges.
6. **Real-time simulated Chat Room**: Switch between conversation panels, typing indicators when matches reply, emoji drawer panel, mock file upload attachments, timestamps, online indicators, and read receipts.
7. **Timeline & Calendar Scheduling**: Month calendar grid highlighting date cells with active slots, reschedule calendar selectors, and star ratings review modal.
8. **Achievements Badges**: Dynamic locks checks on Top Teacher, Active Learner, Community Helper, Skill Master, Knowledge Contributor badges, unlocking visually with alerts when actions are satisfied.
9. **Auth Guard & Session persist**: Registration with password strength visual bars, login checks, credentials validations, and redirect guards on private panels.

---

## 🛠️ Folder Structure

```
learnLoop/
├── css/
│   ├── auth.css              # Form cards and strength meters
│   ├── chat.css              # Messaging bubble feeds, emoji panels, attachments
│   ├── dashboard.css         # Metrics grid, graphs spacing, upcoming items
│   ├── explore.css           # Grid match layouts, compatibility radial SVG borders
│   ├── global.css            # Base variables, dark/light settings, loader screens, custom cursor
│   ├── landing.css           # Hero panels, statistics scrolling counters, carousels
│   ├── profile.css           # Banner overlays, LinkedIn structures, activity posts, experiences list
│   └── requests.css          # Tab selectors, calendar grids, star rating designs
├── js/
│   ├── auth.js               # Sign up checks, password metrics calculations, mock logins
│   ├── chat.js               # Bubble renders, emoji drawers, attachment pings, typing bot replies
│   ├── dashboard.js          # SVG graph plotting, widgets binding, notifications
│   ├── explore.js            # Compatibility calculators, search logic, proposal simulators
│   ├── landing.js            # Scrolling counters, testimonials auto carousel
│   ├── profile.js            # Bio editors, LinkedIn details render, experience logs, posts sharing
│   ├── requests.js           # Approval handlers, days cells generators, book modal, ratings stars
│   └── theme.js              # Theme switcher, cursor moves, scroll progress, database wrapper
├── chat.html                 # Chat workspace view
├── dashboard.html            # Metrics & activity center
├── explore.html              # Search directory
├── index.html                # Main landing page
├── login.html                # Entry login page
├── profile.html              # Profile & achievements showcase
├── register.html             # New account sign up page
├── requests.html             # Scheduling agenda center
└── README.md                 # Project details (this file)
```

---

## 🚀 How to Run the App

Since the application is built entirely as a client-side frontend demo using Vanilla JS/CSS/HTML and local storage database layers:

1. **Direct Browser Execution**:
   - Double-click `index.html` to open the landing page directly in your browser.
   - All page transitions and features will work out of the box!
   
2. **Local Web Server (Recommended)**:
   - For optimal asset resolution and loading speeds, serve the directory using a lightweight web server:
     ```bash
     # Using Python
     python -m http.server 8000
     
     # Or using Node.js
     npm install -g serve
     serve .
     ```
   - Open `http://localhost:8000` or the reported URL.

---

## 💡 How to Test the Interactive Simulation Flows

1. **Register or Login**:
   - Go to `register.html` (via the **Get Started** button on landing).
   - Enter your name, email, and password. Watch the password strength checker progress bar color-shift to green as you fulfill the criteria (number, special character, length).
   - Submit. You will be automatically redirected to `dashboard.html` with a notification telling you that your first badge (**Active Learner**) has been unlocked!
   
2. **Update your LinkedIn Profile**:
   - Go to `profile.html` (via **My Profile** in sidebar).
   - Notice the LinkedIn-style header banner, avatar overlay, professional headline, and connection count stats.
   - Click **Edit Profile** to write an **About Summary**, change location, name, or write a **Professional Headline** (e.g. *"React Developer | Building UX Systems"*).
   - Under **Skills & Endorsements**, add skills you teach (e.g., `JavaScript` at `Expert` level) and skills you want to learn. Note the endorsement count badge next to them!
   
3. **Community Photo Sharing**:
   - Under the **Activity & Photo Sharing** card, click the input bar *"Share a learning moment with a photo..."* to open the creator modal.
   - Write a post caption and select a photo template (Study Setup ☕, Certificate 📜, Whiteboard 🎨, Desktop 💻).
   - Click **Share Post**. The post (complete with caption, large styled SVG mock photo illustration, name, avatar, and headline) immediately updates at the top of your Activity Feed!
   - Click the **Like** button on any feed post to increment and toggle the likes counter.
   
4. **Find Partners**:
   - Navigate to `explore.html` (**Find Partners** in sidebar).
   - Since your profile now wants `Public Speaking` and offers `JavaScript`, notice that mock users (like **Sarah Jenkins**, who teaches `Public Speaking` and wants `HTML/CSS`) rise to the top with a **glowing high compatibility rating** (e.g., 90% compatibility score!).
   - Click **Send Proposal** on her card. A popup opens allowing you to review the barter details. Submit it.
   
5. **Simulated Acceptance**:
   - After submitting, the button on the card will update to `Pending Proposal`.
   - Wait **6 seconds**. An automated simulation engine triggers in the background! You will receive a visual **Toast alert** and notification stating that Sarah Jenkins has approved your proposal.
   - The button on her card will automatically transition to a glowing teal `Active Exchange` button!
   
6. **Chat with Partner**:
   - Click `Active Exchange` or go to `chat.html` (**Messaging** in sidebar).
   - Click on **Sarah Jenkins** in your conversations list.
   - Send her a message (e.g., "Hi Sarah, when are you free?").
   - You will see a `sent` checkmark appear. After **1.5 seconds**, the **Typing indicator** triggers showing `Sarah is typing...`.
   - After another **2.5 seconds**, she replies with a context-aware mock answer!
   - You can also click the paperclip icon to simulate sending a Zip/PDF file, or select the emoji picker to insert emojis.
   
7. **Calendar & Ratings**:
   - Go to `requests.html` (**Requests & Calendar** in sidebar).
   - Select a future day cell on the calendar (a day with no active slots). Click **Schedule Session** to book a session slot for the active day with Sarah Jenkins.
   - A glowing cyan dot will appear on that day in the calendar.
   - In the agenda list below the calendar, click **Complete & Rate** on a session.
   - An interactive 5-star review card modal opens. Highlight 4 or 5 stars, write detailed feedback, and submit.
   - Notice that your dashboard's **Completed Hours** and **Average Rating** are updated, and more achievements are unlocked in your Profile page!
# SkillSync
