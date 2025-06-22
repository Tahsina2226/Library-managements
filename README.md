# 📚 Library Management System  ![Node.js Version](https://img.shields.io/badge/node-%3E%3D16.0.0-brightgreen) ![TypeScript](https://img.shields.io/badge/typescript-%5E4.9.0-blue)

A scalable RESTful API for handling library books, member management, and loan processing.
Implemented using Node.js, TypeScript, Express, and MongoDB.
Comes with comprehensive API documentation via Swagger for easy integration and testing.


## 📌 Introduction

This project provides a backend RESTful API server built with Express and TypeScript to manage a library system.  
It supports functionalities such as book management, member registration, and lending operations (coming soon).  
Data persistence is handled by MongoDB via Mongoose.



---

## ✨ Features

- **Book Management**
  - Create, read, update, and delete books
  - Genre filtering and sorting
  - ISBN validation
- **Borrowing System**
  - Quantity validation
  - Automatic availability updates
- **Reporting**
  - Borrowed books summary
  - Aggregation pipeline analytics
- **Technical**
  - TypeScript support
  - Mongoose schema validation
  - Error handling middleware

---

## 🛠️ Installation

### 1. Clone & Install  
```bash
git clone https://github.com/Tahsina2226/Library-managements.git
cd Library-managements
npm install
```

### 2. Configure Environment  
Create `.env` in the root directory:  
```env
DB_USER=*****
DB_PASS=*****
PORT=5000
MONGO_URI=your_mongodb_connection_string

```

### 3. Run the Server  
```bash
npm run dev  
npm start  
```

🔹 **Access the server:** `http://localhost:5000`  

---
---

## 🚀 Usage

### Development Mode
```bash
npm run dev
```
Access the server at: http://localhost:5000

Production Mode
```bash

npm start
```
Testing
```bash

npm test

```
---

## 📡 API Documentation  
Explore endpoints interactively with :  
🌐 [http://localhost:5000/](http://localhost:5000/api/)  

---
## 🌐 Live Demo

Check out the live Library Management System application here:  
[https://library-management-system-five-nu.vercel.app/](https://library-management-system-five-nu.vercel.app/)



---

## 🗂 Project Structure  
```bash
├── 📁 .vercel/
├── 📁 dist/
├── 📁 node_modules/
├── 📁 src/
│   ├── 📁 apps/
│   ├── 📁 models/
│   │   ├── 📄 Books.ts
│   │   └── 📄 borrow.model.ts
│   ├── 📁 routes/
│   │   ├── 📄 bookroutes.ts
│   │   └── 📄 borrow.routes.ts
│   ├── 📄 app.ts
│   └── 📄 server.ts
├── 📄 .env
├── 📄 .gitignore
├── 📄 eslint.config.js
├── 📄 log.txt
├── 📄 package-lock.json
├── 📄 package.json
├── 📄 README.md
├── 📄 tsconfig.json
└── 📄 vercel.json
```


---

## 📜 Scripts  
| Command           | Description                          |
|-------------------|--------------------------------------|
| `npm run dev`     | Start dev server (hot-reload)        |
| `npm start`       | Start production server              |
| `npm run build`   | Compile TypeScript to `dist/`        |
| `npm run lint`    | Run ESLint                           |
| `npm run test`    | Run tests (WIP)                      |

---

## 🛠 Dependencies  
### Core  
- `express` – Web framework  
- `mongoose` – MongoDB



## 🔌 API Endpoints

## 📡 API Endpoints

| Method | Endpoint           | Description                 |
|--------|--------------------|-----------------------------|
| POST   | `/api/books`       | Create a new book           |
| GET    | `/api/books`       | Get all books (supports filter/sort) |
| GET    | `/api/books/:bookId` | Get a book by ID           |
| PUT    | `/api/books/:bookId` | Update a book              |
| DELETE | `/api/books/:bookId` | Delete a book              |
| POST   | `/api/borrow`      | Borrow a book               |
| GET    | `/api/borrow`      | Get borrowed books summary  |

---

## 📋 Data Models

### 📘 Book

| Field       | Type     | Required | Notes                                               |
|-------------|----------|----------|-----------------------------------------------------|
| title       | string   | ✅        | Title of the book                                   |
| author      | string   | ✅        | Book author                                        |
| genre       | string   | ✅        | One of: FICTION, NON_FICTION, SCIENCE, HISTORY, BIOGRAPHY, FANTASY |
| isbn        | string   | ✅        | Unique ISBN number                                 |
| description | string   | ❌        | Short description                                  |
| copies      | number   | ✅        | Must be a positive integer                         |
| available   | boolean  | ❌        | Defaults to `true`                                |

### 📗 Borrow

| Field    | Type     | Required | Notes                 |
|----------|----------|----------|-----------------------|
| book     | ObjectId | ✅        | References a Book      |
| quantity | number   | ✅        | Must be a positive number |
| dueDate  | Date     | ✅        | Borrow return deadline  |


#### 📥 Response Example

```json
{
  "success": true,
  "message": "Book created successfully",
  "data": {
    "_id": "64f123abc4567890def12345",
    "title": "The Theory of Everything",
    "author": "Stephen Hawking",
    "genre": "SCIENCE",
    "isbn": "9780553380163",
    "copies": 5,
    "available": true,
    "createdAt": "2024-11-19T10:23:45.123Z",
    "updatedAt": "2024-11-19T10:23:45.123Z"
  }
}
```




 
## 🛠 Development

### Available Scripts

| Command           | Description            |
|-------------------|------------------------|
| `npm run dev`     | Start the development server with hot reloading |
| `npm run build`   | Compile TypeScript to JavaScript |
| `npm run lint`    | Run ESLint to check code quality |
| `npm run format`  | Format code using Prettier |
| `npm test`        | Run test suites         |


---

## 🧩 Troubleshooting

### Connection Issues
- Ensure MongoDB service is running and accessible.
- Verify that the connection string in your `.env` file (`MONGO_URI`) is correct.

### Validation Errors
- Make sure your request payload matches the required schema.
- Check that all mandatory fields are included in your requests.

### TypeScript Compile Errors
- Clean and rebuild the project by running `npm run build`.
- Verify that your type annotations and interfaces are correctly defined.
- Check for any missing or incompatible types in your code.




## 👥 Contributors  
- **Tahsina Tanvin** – [@Tahsina2226](https://github.com/Tahsina2226)


---

## 📝 License  
MIT © 2024 [Tahsina Tanvin](https://github.com/Tahsina2226).  



---


