# BlackBox

A real-time multiplayer elimination quiz game built with Node.js and Express. Players answer questions each round, and wrong answers eliminate them — last one standing wins!

---

## How It Works

- A game **round starts** and all players receive a question
- Players **submit their answers** before time runs out
- Wrong answers → player is **eliminated**
- The game continues until one player remains
- A **leaderboard** tracks scores and standings

---

## Tech Stack

| Layer | Technology |
|---|---|
| Runtime | Node.js |
| Framework | Express.js |
| Architecture | MVC (Routes → Controllers) |

---

## Project Structure

```
BlackBox/
├── controllers/
│   └── gameController.js      # Game logic (start, submit, eliminate, leaderboard)
├── routes/
│   └── gameRoutes.js          # API route definitions
├── app.js                     # Entry point
└── README.md
```

---

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/game/start` | Start a new game round |
| `POST` | `/game/submit` | Submit a player's answer |
| `POST` | `/game/force-eliminate` | Manually eliminate a player |
| `POST` | `/game/test` | Test and generate output |
| `GET` | `/game/leaderboard` | Get current leaderboard |

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org) (v16 or above recommended)
- npm (comes with Node.js)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/06Nandhini/BlackBox.git

# 2. Navigate into the project
cd BlackBox

# 3. Install dependencies
npm install

# 4. Start the server
node app.js
```


---

## Usage Example

**Start a game:**
```bash
POST /game/start
```

**Submit an answer:**
```bash
POST /game/submit
Content-Type: application/json

{
  "playerId": "player_1",
  "answer": "your answer here"
}
```

**View leaderboard:**
```bash
GET /game/leaderboard
```



> Built with Node.js — because JavaScript deserved wings. 🚀
