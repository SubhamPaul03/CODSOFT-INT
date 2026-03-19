# 🤖 CODSOFT AI Internship Projects

![Internship](https://img.shields.io/badge/Internship-CODSOFT-blue?style=for-the-badge)
![Domain](https://img.shields.io/badge/Domain-Artificial%20Intelligence-green?style=for-the-badge)
![Language](https://img.shields.io/badge/Language-JavaScript%20%7C%20HTML%20%7C%20CSS-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

> A collection of three fully functional AI projects built during the **CODSOFT Artificial Intelligence Internship**. Each project demonstrates a core concept in AI — from natural language processing and game theory to recommendation algorithms.

---

## 📋 Table of Contents

- [About the Internship](#about-the-internship)
- [Projects](#projects)
  - [Task 1 — Rule-Based Chatbot](#task-1--rule-based-chatbot)
  - [Task 2 — Tic-Tac-Toe AI](#task-2--tic-tac-toe-ai)
  - [Task 3 — Recommendation System](#task-3--recommendation-system)
- [Tech Stack](#tech-stack)
- [How to Run](#how-to-run)
- [Key Learnings](#key-learnings)
- [Connect](#connect)

---

## 🎓 About the Internship

This repository contains all tasks completed as part of the **CODSOFT AI Internship Program**. The internship focused on building practical AI applications that reinforce foundational concepts including:

- Natural Language Processing (NLP)
- Search Algorithms & Game Theory
- Collaborative and Content-Based Filtering
- Algorithm design and optimization

Each project is built with vanilla **HTML, CSS, and JavaScript** — no external frameworks or libraries — making them lightweight, portable, and easy to run directly in any browser.

---

## Projects

---

### Task 1 — Rule-Based Chatbot

📁 `Task1-Chatbot/chatbot.html`

#### 📌 Description
A conversational chatbot agent named **AXIOM** that responds to user inputs using predefined rules. The bot uses regex-based **pattern matching** to identify user intent and deliver contextually appropriate responses.

#### 🧠 AI Concepts Used
- **Intent Classification** — Messages are matched against 13 rule categories (greetings, farewells, jokes, math, time queries, etc.)
- **Pattern Matching** — Regular expressions scan input for keywords and phrase structures
- **Session Memory** — The bot remembers the user's name across the conversation
- **Dynamic Response Generation** — Some rules compute real answers (e.g., live clock, arithmetic evaluation)
- **Fallback Handling** — Unrecognized inputs trigger randomised fallback responses

#### ✨ Features
- 13 intent rules covering greetings, jokes, math, time, date, identity, and more
- Real-time arithmetic evaluation (`15 × 8`, `100 / 4`, etc.)
- Randomised responses per intent for variety
- Typing indicator animation
- Suggestion chips for quick interaction
- Retro terminal UI with CRT scanline aesthetic

---

### Task 2 — Tic-Tac-Toe AI

📁 `Task2-TicTacToe-AI/tictactoe-ai.html`

#### 📌 Description
An unbeatable Tic-Tac-Toe AI agent that plays against a human player. The AI uses the **Minimax algorithm** enhanced with **Alpha-Beta Pruning** to evaluate every possible game state and always select the optimal move.

#### 🧠 AI Concepts Used
- **Minimax Algorithm** — Recursively explores the full game tree, assuming optimal play from both sides. Terminal states are scored: AI win = `+10 - depth`, Player win = `depth - 10`, Draw = `0`
- **Alpha-Beta Pruning** — Cuts branches that cannot influence the final decision, reducing nodes searched from O(b^d) to O(b^(d/2)) in the best case
- **Game Tree Search** — All 9! = 362,880 possible game states are evaluated
- **Heuristic Mode** — Medium difficulty uses hand-coded heuristics (win → block → center → corner)

#### ✨ Features
- 3 difficulty levels: Easy (random), Medium (heuristic), Hard (unbeatable Minimax)
- Live **node counter** showing α-β pruning efficiency in real time
- Score tracker across multiple games
- Swap first move (test if you can beat the AI going second)
- Auto-restart after each round
- Retro green-phosphor terminal UI

#### 📊 Algorithm Complexity
| Mode | Strategy | Nodes Searched |
|------|----------|----------------|
| Easy | 60% random | ~0 |
| Medium | Heuristic rules | ~0 |
| Hard | Full Minimax + α-β | ~500–5000 |

---

### Task 3 — Recommendation System

📁 `Task3-Recommendation-System/recommendation-system.html`

#### 📌 Description
A personalised movie recommendation engine named **CINE·LENS** that suggests films to users based on their viewing history. Supports three recommendation algorithms selectable at runtime.

#### 🧠 AI Concepts Used
- **Collaborative Filtering (User-User)** — Computes **Pearson Correlation** between users' rating vectors to find taste-similar viewers, then predicts unseen film scores as a similarity-weighted average
- **Content-Based Filtering** — Builds a personal tag & genre preference profile from rated films, then scores unseen films by attribute overlap
- **Hybrid Filtering** — Normalises both score vectors independently and blends them (55% collaborative + 45% content) for balanced recommendations
- **Cosine Similarity** — Used as an alternative similarity metric

#### ✨ Features
- 5 pre-built user profiles with distinct taste signatures
- 20 curated films with genre, tags, year, and descriptions
- Switch algorithms at runtime — recommendations update instantly
- Rate any film by clicking its card → model updates in real time
- User similarity bars visualising Pearson correlation scores
- Genre filter chips for category drilling
- Match % score bar on every recommendation card
- Editorial magazine UI design

#### 📐 Pearson Correlation Formula
```
sim(A,B) = Σ(rA − μA)(rB − μB) / √[Σ(rA−μA)² · Σ(rB−μB)²]
```
Where `rA`, `rB` are ratings and `μA`, `μB` are each user's mean rating.

---

## 🛠 Tech Stack

| Technology | Usage |
|------------|-------|
| HTML5 | Structure and layout |
| CSS3 | Styling, animations, responsive design |
| Vanilla JavaScript | AI logic, DOM manipulation, state management |
| Regex | Pattern matching in chatbot |
| Google Fonts | Typography (Orbitron, DM Serif, Share Tech Mono) |

> **No frameworks. No libraries. No dependencies.** Every project runs as a single `.html` file directly in the browser.

---

## 🚀 How to Run

### Option 1 — Open directly in browser (simplest)
```
1. Download or clone this repository
2. Navigate to any task folder
3. Double-click the .html file
4. Opens instantly in your browser — no setup needed
```

### Option 2 — Clone via Git
```bash
git clone https://github.com/YOUR_USERNAME/CODSOFT.git
cd CODSOFT

# Open any project
open Task1-Chatbot/chatbot.html
open Task2-TicTacToe-AI/tictactoe-ai.html
open Task3-Recommendation-System/recommendation-system.html
```

### Option 3 — VS Code Live Server
```
1. Open folder in VS Code
2. Install the "Live Server" extension
3. Right-click any .html file → "Open with Live Server"
```

---

## 📚 Key Learnings

- Implemented **Minimax + Alpha-Beta Pruning** from scratch and observed the dramatic reduction in nodes searched
- Understood the difference between **model-based** (content) and **memory-based** (collaborative) recommendation approaches
- Learned how **Pearson Correlation** captures relative taste similarity better than raw cosine distance for sparse rating data
- Built production-quality UIs entirely in vanilla CSS with animations, without any UI libraries
- Practiced **modular JavaScript** architecture — separating data, algorithm logic, and rendering cleanly

---

## 📁 Repository Structure

```
CODSOFT/
│
├── README.md
│
├── Task1-Chatbot/
│   └── chatbot.html          # Rule-based NLP chatbot
│
├── Task2-TicTacToe-AI/
│   └── tictactoe-ai.html     # Minimax + Alpha-Beta Pruning AI
│
└── Task3-Recommendation-System/
    └── recommendation-system.html  # Collaborative + Content-based filtering
```

---

## 🤝 Connect

Made with dedication during the **CODSOFT AI Internship**.

[![GitHub](https://img.shields.io/badge/GitHub-YOUR__USERNAME-black?style=flat-square&logo=github)](https://github.com/YOUR_USERNAME)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/YOUR_PROFILE)

---

*© 2024 · CODSOFT AI Internship · All projects are open source*
