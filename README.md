# Annapoorana Kitchen - WhatsApp Food Ordering Bot 🍛

A smart, automated food ordering system built with **FastAPI**, **Twilio WhatsApp API**, and **ngrok**. This bot handles the entire customer journey from menu browsing to order confirmation.

## 🚀 Features
- **Interactive Menu:** Browse categories like Starters, Main Course, Desserts, and Beverages.
- **Persistent Cart:** Add or remove items dynamically; the bot remembers your cart throughout the session.
- **Smart Typo Handling:** Intelligent "Fuzzy Matching" logic that recognizes common spelling mistakes (e.g., 'mancoser' -> Main Course).
- **11-Step Checkout Flow:** A structured process including OTP verification, Name, Address, and Pincode collection.
- **Live Server Status:** Integrated health-check route to verify server status via browser.

---

## 📁 Project Structure
```text
Annapoorana_bot/
├── main.py              # Main application logic and API routes
├── requirements.txt     # List of required Python packages
├── README.md            # Project documentation and setup guide
└── .gitignore           # Files to exclude from GitHub (venv, ngrok.exe)

🛠️ How to Setup and Run
1. Clone the Project
Download this repository as a ZIP file and extract it to your Desktop.

2. Setup Virtual Environment
Open your VS Code Terminal and run:

Bash
python -m venv venv
.\venv\Scripts\activate
3. Install Dependencies
Install the required libraries using pip:

Bash
pip install -r requirements.txt
4. Start the Application
Run the Uvicorn server:

Bash
uvicorn main:app --reload
Your server is now live locally at http://127.0.0.1:8000

5. Setup the ngrok Tunnel
Download ngrok and place the .exe in your project folder.

In a new terminal, run:

Bash
ngrok http 8000
Copy the https://... Forwarding URL provided by ngrok.

6. Configure Twilio Webhook
Log in to your Twilio Console.

Go to Messaging > Settings > WhatsApp Sandbox Settings.

In the "When a message comes in" field, paste your ngrok URL and add /whatsapp at the end.

Example: https://your-id.ngrok-free.app/whatsapp

Set the method to HTTP POST and click Save.

🧪 Testing the Bot
Send "Hi" to your Twilio Sandbox number.

Try a typo: Send "mancorse" to see the smart correction logic.

Complete an order: Type "Checkout" to start the 11-step verification process.

🛠️ Tech Stack
Backend: Python, FastAPI

API: Twilio WhatsApp Business API

Tunneling: ngrok

Server: Uvicorn
