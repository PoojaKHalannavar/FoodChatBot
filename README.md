A Chatbot for online food orders using Dialogflow 
===================
A food ordering chatbot built with Dialogflow ES and a FastAPI backend, utilizing a MySQL database and a responsive frontend. 

The chatbot allows users to place new orders and track existing ones. The FastAPI backend handles user requests, processes orders, and communicates with the MySQL database for order management. The responsive frontend ensures a seamless user experience.

1) New Order: Sample Conversation
```
User: Hey
Bot: Hello, How can I assist? You can say: "New Order" or "Track Order"
User: New Order
Bot: What would you like to order? For example, you can say "2 pizzas, one vada pav."
Only these items are available: Vada Pav, Pav Bhaji, Mango Lassi, Pizza, Rava Dosa, Masala Dosa, Samosa.
User: I will take 1 Pav Bhaji and 2 Masala Dosas
Bot: Added 1 Pav Bhaji and 2 Masala Dosas. Anything else?
User: Yes, add one Mango Lassi.
Bot: Sure. Your order now has 1 Pav Bhaji, 2 Masala Dosas, and 1 Mango Lassi. Anything else?
User: Actually, remove the Pav Bhaji.
Bot: Got it. Now your order has 2 Masala Dosas and 1 Mango Lassi. Anything else?
User: Nope, that's all.
Bot: Great! Your order is placed. Order ID #52. Your total is $15, payable at delivery.
```

2) Track Order: Sample Conversation
```
User: Track Order
Bot: What is your order id?
User: 46
Bot: Order #46, is in transit
User: How about 42
Bot: Order #42 is delivered
```

Directory structure
===================
backend: Contains Python FastAPI backend code

db: contains the dump of the database. you need to import this into your MySQL db by using MySQL workbench tool

frontend: website code

Install these modules
======================

pip install mysql-connector

pip install "fastapi[all]"

OR just run pip install -r requirements.txt to install both in one shot

To start fastapi backend server
================================
1. Go to backend directory in your command prompt
2. Run this command: uvicorn main:app --reload

ngrok for https tunneling
================================
1. To install ngrok, go to https://ngrok.com/download and install ngrok version that is suitable for your OS
2. Extract the zip file and place ngrok.exe in a folder.
3. Open windows command prompt, go to that folder and run this command: ngrok http 80000

NOTE: ngrok can timeout. you need to restart the session if you see session expired message.

Project Snapshots
===================

