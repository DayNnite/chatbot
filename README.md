Chatbot Gateway Server
Overview
This project hosts a lightweight API gateway that validates clients and dynamically injects a white-labeled chatbot widget.

The goal is to control access to the widget for paying customers using a client ID and access token system.

Features
Gateway script (gateway.js) that authenticates clients before loading the chatbot.

Token generation script (generateToken.js) for issuing access tokens.

Server built with Node.js and Express.js.

Supports easy deployment (e.g., Render, Vercel).

Includes control over client permissions.

Folder Structure
server.js: Main Express server file.

widget.js: Widget loader file.

generateToken.js: Script to generate tokens (optional for scaling later).

note: Documentation notes.

vercel.json: Deployment settings for Vercel.

package.json: Node dependencies and scripts.

node_modules/: Installed packages.

How It Works
Clients embed the gateway script:

html
Copy
Edit
<script src="https://your-deployed-server.com/gateway.js?clientId=client123&accessToken=abc123"></script>
The server verifies the clientId and accessToken.

If valid, the real chatbot widget (widget.js) is injected onto the client’s site.

Invalid credentials result in no widget being loaded.

Setup Instructions
Clone the repo:

bash
Copy
Edit
git clone [repo-url]
cd chatbot-main
Install dependencies:

bash
Copy
Edit
npm install
Run the server locally:

bash
Copy
Edit
node server.js
Deploy to Render or Vercel for production.

Future Plans
Integrate JWT tokens for more secure authentication.

Add an admin dashboard to manage clients.

Improve error handling and access revocation.
