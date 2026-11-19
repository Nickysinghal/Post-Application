# BackendPostApp

A simple full-stack post application for uploading images with captions and viewing them in a responsive feed.

## Features

- Create a post with an image and caption
- Upload images through ImageKit
- Store post data in MongoDB
- View posts in a responsive dark-themed feed

## Project structure

```text
Backend/    Express API, MongoDB model, and ImageKit upload service
Frontend/   React and Vite client
```

## Requirements

- Node.js
- MongoDB connection
- ImageKit account and private key

## Configuration

Create `Backend/.env` with:

```env
MONGO_URI=your_mongodb_connection_string
IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
```

## Running locally

Install dependencies:

```bash
cd Backend
npm install

cd ../Frontend
npm install
```

Start the backend in one terminal:

```bash
cd Backend
node server.js
```

Start the frontend in another terminal:

```bash
cd Frontend
npm run dev
```

The backend runs on `http://localhost:3000`. Vite prints the frontend URL in the terminal.

## API endpoints

| Method | Endpoint | Description |
| --- | --- | --- |
| `POST` | `/create-post` | Upload an image and create a captioned post |
| `GET` | `/posts` | Retrieve all posts |
