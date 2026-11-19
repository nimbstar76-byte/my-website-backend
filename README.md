# my-website-backend
Node.js backend API for website form submissions and WhatsApp notifications.

package.json
{
  "name": "my-website-backend",
  "version": "1.0.0",
  "type": "module",
  "scripts": {
    "start": "node server.js"
  },
  "dependencies": {
    "express": "^4.21.2"
  }
}

server.js

import express from "express";

const app = express();
const PORT = process.env.PORT || 3000;

app.use(express.json());

app.get("/", (req, res) => {
  res.send("My Website Backend is Running!");
});

app.get("/api/health", (req, res) => {
  res.json({
    success: true,
    message: "Backend is working"
  });
});

app.listen(PORT, () => {
  console.log(`Server running on port ${PORT}`);
});

