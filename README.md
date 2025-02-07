# AI-Powered Chatbot for Supplier and Product Information

## Overview
This project is an AI-powered chatbot that enables users to query a product and supplier database using natural language. It leverages LangGraph for workflow management and integrates an open-source LLM for summarizing supplier and product details.

## Project Links
- **GitHub Repository:** [AI-Powered Chatbot](https://github.com/s11saurabh/AI-Powered_Chatbot)
- **Deployed Application:** [Live Chatbot](https://saibarathr.github.io/gemini-bot-react/)

<img width="1464" alt="image" src="https://github.com/user-attachments/assets/8d70b31e-22ed-47aa-a4c8-4cbc00e3c092" />
<img width="1464" alt="image" src="https://github.com/user-attachments/assets/680f3d55-ad25-43fb-9236-f9ed93a048c5" />

## Features
- **Natural Language Query Support**: Users can ask queries like "Show me all products under brand X" or "Which suppliers provide laptops?"
- **Efficient Data Retrieval**: Fetches relevant information from a MySQL/PostgreSQL database.
- **AI-Powered Summarization**: Uses an LLM to enhance responses.
- **User-Friendly Interface**: Built with React, featuring a chat UI with query history.
- **Error Handling**: Gracefully manages missing or incorrect queries.

## Tech Stack
### **Frontend**
- **React.js**: User interface development.
- **Material UI/Tailwind CSS**: Styling components.
- **Axios**: API calls to the backend.
- **Redux/Context API**: State management.

### **Backend**
- **Python (FastAPI/Flask)**: REST API implementation.
- **LangGraph**: Agent workflow framework for chatbot interactions.
- **Open-Source LLM**: Hugging Face's GPT-2/GPT-3/LLaMA 2 for summarization.

### **Database**
- **MySQL/PostgreSQL**: Stores supplier and product data.

## Folder Structure
```
AI-Powered_Chatbot/
│── backend/
│   ├── fixtures/
│   │   ├── BotResponse.json
│   ├── app.js
│   ├── routes.js
│   ├── package.json
│── frontend/
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   │   ├── bot.png
│   │   ├── components/
│   │   │   ├── Message.js
│   │   ├── App.js
│   │   ├── index.js
│   │   ├── reportWebVitals.js
│   │   ├── setupTests.js
│   ├── package.json
│   ├── package-lock.json
│── .gitignore
│── README.md
```

## Installation & Setup
### **Prerequisites**
Ensure you have the following installed:
- **Node.js** & **npm/yarn** (for frontend)
- **Python** (for backend)
- **MySQL/PostgreSQL** (for database)

### **Backend Setup**
```sh
cd backend
pip install -r requirements.txt
python app.py
```

### **Frontend Setup**
```sh
cd frontend
npm install
npm start
```

### **Database Setup**
1. Create a MySQL/PostgreSQL database.
2. Run SQL schema script to create tables:
```sql
CREATE TABLE Products (
    ID INT PRIMARY KEY,
    name VARCHAR(255),
    brand VARCHAR(100),
    price DECIMAL(10,2),
    category VARCHAR(100),
    description TEXT,
    supplier_ID INT
);

CREATE TABLE Suppliers (
    ID INT PRIMARY KEY,
    name VARCHAR(255),
    contact_info TEXT,
    product_categories TEXT
);
```
3. Populate with sample data.

## Usage
1. Open the deployed application or run it locally.
2. Type a query in the chatbot.
3. The chatbot fetches data from the database and enhances responses with an LLM.
4. Results are displayed in a conversational format.

## Evaluation Criteria
- **Functionality**: Completeness and accuracy of chatbot responses.
- **Code Quality**: Clean, modular, and well-documented code.
- **Scalability**: Efficient query handling and performance.
- **UI/UX**: Responsive and intuitive interface.

## Optional Enhancements (Bonus Features)
- **Authentication (JWT-based login)**
- **Product Comparisons**
- **Chatbot Memory (User Preferences Recall)**
- **Analytics Dashboard (Query Tracking)**

## Contributors
- **Saurabh** ([GitHub](https://github.com/s11saurabh))

## License
This project is licensed under the MIT License.


