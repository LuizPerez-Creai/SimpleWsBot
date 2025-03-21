# SimpleWsBot

SimpleWsBot is a WhatsApp chatbot built using Node.js, Baileys library, Express, and Socket.IO, designed to automate interactions by responding to user queries, sending automated replies, and providing useful information.

## Features

- **WhatsApp Integration** using the Baileys library to manage connection, authentication, and messaging.
- **Dynamic QR Code generation** for easy connection setup.
- **Predefined automated responses**:
  - Schedule appointments
  - Provide contact numbers
  - Share location details
  - Offer general assistance
- **Socket.IO Integration** for real-time QR code scanning interface.
- **Express Server** with REST endpoints for manual message sending, generating new QR codes, and disconnecting the session.

## Tech Stack

- Node.js
- Express
- Baileys
- Socket.IO
- QR Code
- File upload handling
- Cors & Body-parser Middleware

## Installation

1. **Clone this repository:**

```bash
git clone https://github.com/HidenLacan/SimpleWsBot.git
cd SimpleWsBot
```

2. **Install dependencies:**

```bash
npm install
```

## Usage

1. **Run the server:**

```bash
npm start
```

2. **Scan the QR Code:**

Visit `http://localhost:8000/scan` to access the interface and scan the dynamically generated QR code to authenticate the WhatsApp session.

## API Endpoints

- `GET /send-message?number=<number>&message=<message>`: Send a manual WhatsApp message.
- `POST /disconnect`: Disconnect the active WhatsApp session.
- `POST /generate-qr`: Generate a new QR code for reconnecting WhatsApp.

## Project Structure

```
SimpleWsBot/
├── client
│   ├── assets (images and frontend assets)
│   └── index.html (QR scanning interface)
├── session_auth_info (authentication data)
├── main.js (application entry point)
└── package.json
```

## Contributing

Contributions are welcome! Please fork the repository, create your feature branch, and submit a pull request.

## License

This project is open-source, available under the MIT License.

