# URL Shortener Project

A full-stack URL shortener built with React on the frontend and Express + MongoDB on the backend. The app allows users to shorten long URLs, view the saved links, and delete them from the database.

## Features

- Shorten long URLs into a compact short code
- Store original URLs and generated codes in MongoDB
- View all shortened URLs in the dashboard
- Delete saved records
- Frontend built with Vite + React
- Backend built with Express and Mongoose

## Tech Stack

- Frontend: React, Vite, Axios
- Backend: Node.js, Express
- Database: MongoDB with Mongoose

## Project Structure

```bash
URL/
├── Client/
│   ├── src/
│   ├── public/
│   ├── package.json
│   ├── vite.config.js
│   └── index.html
├── Server/
│   ├── src/
│   ├── Server.js
│   └── package.json
├── README.md
└── .gitignore
```

## Prerequisites

Before running the project, make sure you have:

- Node.js installed
- MongoDB running locally or a MongoDB Atlas connection string
- npm installed

## Setup

### 1. Install frontend dependencies

```bash
cd Client
npm install
```

### 2. Install backend dependencies

```bash
cd Server
npm install
```

### 3. Configure environment variables

Create a `.env` file inside the `Server` folder:

```env
MONGO_URI=mongodb://127.0.0.1:27017/url-shortener
```

If you are using MongoDB Atlas, replace the value with your connection string.

## Run the Application

### Start the backend server

```bash
cd Server
node Server.js
```

The server runs on:

```bash
http://localhost:3000
```

### Start the frontend

```bash
cd Client
npm run dev
```

The frontend runs on:

```bash
http://localhost:5173
```

## API Endpoints

### Create shorten URL

```http
POST /api/url
```

Request body:

```json
{
  "url": "https://example.com/very/long/url"
}
```

### Get all URLs

```http
GET /api/url

### Delete a URL

```http
DELETE /api/url/:id
```

## Notes

- The frontend connects to the backend at `http://localhost:3000`.
- The backend uses CORS to allow requests from the React app.
- The database connection is established in `Server/src/config/db.js`.

## Future Improvements

- Add URL redirect functionality for short codes
- Add copy-to-clipboard feature for short links
- Add validation and duplicate URL handling
- Improve UI design and analytics

## License

This project is for educational and learning purposes.
 