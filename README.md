# 📚 Flashcard v3

A full-stack flashcard application that allows users to create, manage, and play with flashcard decks. This project consists of a **React Frontend**, a **Node.js & Express API**, and a **MySQL Backend**.

---

## 📋 Table of Contents
- [Features](#-features)
- [Technologies Used](#️-technologies-used)
- [Installation & Setup](#️-installation--setup)
- [API Endpoints](#-api-endpoints)
- [Usage Guide](#-usage-guide)
- [Future Enhancements](#-future-enhancements)
- [Author](#-author)
- [TODO:](#todo)

---

## 🚀 Features
- **Deck Management (`/decks`, `/decks/:id`)** – Browse all available decks, view specific deck details, and create, edit, or delete flashcard decks and their contents.
- **Interactive Study & Game Mode (`/playgame`, `/playgame/:id`)** – Select a deck, confirm your session (`/playgame/confirmation/:id`), and test your knowledge by flipping through flashcards.
- **Post-Game Results (`/results`)** – Review your performance and study outcomes after completing a flashcard session.
- **Fast Add via CSV Upload (`/fastadd`)** – Quickly bulk-create and upload new flashcard decks using CSV files.
- **Quick Downloads** – Export decks to a `.json` file for quick backups or offline editing.
- **REST API** – Fetch, create, update, and delete decks seamlessly.

---

## 🛠️ Technologies Used

### **Frontend**
- **React (`^19.0.0`) & React DOM (`^19.0.0`)** – Component-based UI
- **React Router DOM (`^7.18.5`)** – Client-side routing and navigation
- **React Scripts (`5.0.1`)** – Create React App build and development scripts
- **React Toastify (`^11.2.0`)** – Clean error and status notifications
- **Fetch API** – Asynchronous API calls
- **CSS** – Custom responsive styling

### **Backend**
- **Node.js** – JavaScript runtime environment
- **Express (`^5.3.0`)** – RESTful API routing and middleware
- **MySQL2 (`^3.24.6`)** – MySQL database client for persistent storage
- **CORS (`^2.8.6`)** – Cross-Origin Resource Sharing middleware
- **dotenv (`^18.0.10`)** – Environment variable management

---

## ⚙️ Installation & Setup

### **1. Clone the repository**
```sh
git clone https://github.com/TylerRollo/flashcard-v3.git
cd flashcard-v3
```

### **2. Install dependencies**

#### **Backend**
```sh
cd backend
npm install
```

#### **Frontend**
```sh
cd frontend
npm install
```

### **3. Set up environment variables**
Create a `.env` file in the `backend` directory and configure your database credentials:
```env
MYSQL_HOST='your_host'
MYSQL_USER='your_user'
MYSQL_PASSWORD='your_password'
MYSQL_DATABASE='your_db'
PORT=your_port_number
```

### **4. Start the backend**
```sh
cd backend
npm start
```

### **5. Start the frontend**
```sh
cd frontend
npm start
```

---

## 📡 API Endpoints

### **Decks**
- `GET /api/decks` – Fetch all decks
- `GET /api/decks/:id` – Fetch a single deck by ID
- `POST /api/decks` – Create a new deck
- `PUT /api/decks/:id` – Update deck name or description
- `DELETE /api/decks/:id` – Delete a deck

---

## 🎮 Usage Guide
1. **Start at Home (`/home`)** – Navigate to your deck library or jump straight into a study session.
2. **Manage Your Decks (`/decks` & `/decks/:id`)** – View all decks, inspect individual cards inside a deck, and add, edit, or remove decks.
3. **Bulk Upload via Fast Add (`/fastadd`)** – Upload a CSV file to rapidly generate a new deck of flashcards.
4. **Play the Game (`/playgame`)** – Choose a deck to study, confirm your game settings (`/playgame/confirmation/:id`), and flip through the cards (`/playgame/:id`).
5. **Review Results (`/results`)** – Check your session results once you finish a deck, then retry to reinforce learning or pick a new deck.

---

## 📌 Future Enhancements
- Progress tracking and long-term study statistics
- Categorizing or tagging cards within a deck
- Full multi-user authentication and account management
- Cloud deployment and hosting

---

## 👨‍💻 Author
[GitHub](https://github.com/TylerRollo) | [LinkedIn](https://linkedin.com/in/tyler-rollo)

---

## TODO:
- [ ] Add multiple users support (user-specific decks and data isolation)
- [ ] Set up Version Control environments (`dev`, `test`, `prod`)
- [ ] Input validation on anything that calls the API (CSV/JSON uploads, deck/card names, form inputs)
- [ ] Implement Session Cookies to persist user/session data (replace passing state variables via `navigate`)
- [ ] Search/filter decks by name

### Security Checks (TODO:)
- [ ] Strict file type and schema validation for CSV and `.json` uploads
- [ ] Secure file/data handling when uploading to the cloud
- [ ] Service availability and rate limiting
- [ ] Database security (parameterized queries, least-privilege DB user)
- [ ] User authorization and route protection
- [ ] Secure cookie configuration (`HttpOnly`, `Secure`, `SameSite`)
