# Two-Player Game with Kafka and Socket.io

This project is a simple two-player game developed with Node.js, utilizing Kafka for real-time state synchronization and Socket.io for real-time communication between clients and the server. The game allows two players to move their avatars up or down on a webpage, with each player's position being synchronized across both clients in real-time.

## Features

- Real-time player state synchronization with Kafka
- Real-time communication with Socket.io
- Express.js for serving static files and views
- EJS for templating
- Environment-based configuration

## Prerequisites

Before you start, ensure you have the following installed on your system:

- Node.js (v14 or later recommended)
- npm (comes with Node.js)
- Access to a Kafka cluster (this project uses Upstash Kafka)

## Getting Started

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/your-repository-name.git
cd your-repository-name
```

2. **Configure the environment variables**
Rename the .env.example file to .env and fill in your Kafka and other configuration details.

```bash
npm start
```

Your game should now be running on http://localhost:3000 open a browser to play.

***Game Play***
Open http://localhost:3000 in two different browser windows or tabs. Use the arrow keys (ArrowUp and ArrowDown) for one player and W/S for the other player to move the avatars up and down.


***Architecture***
This game uses a Node.js server for the backend, Kafka for messaging, and Socket.io for frontend communication. Player movements are sent from the client to the server via Socket.io, then broadcasted to Kafka, and finally, consumed from Kafka and broadcasted to all connected clients to synchronize the game state.

***Contributing***
Contributions are welcome! Please feel free to submit a pull request.