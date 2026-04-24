# Minimal MERN Student App

## Structure

- `server` - Node.js, Express, MongoDB (Mongoose), Student CRUD API
- `client` - React (Vite), Axios UI for add/list/delete students

## Backend setup

1. Go to `server`
2. Install dependencies:
   - `npm install`
3. Create `.env` and paste your credentials
4. Run server:
   - `node index.js`

Server runs at `http://localhost:5000`

## Frontend setup

1. Go to `client`
2. Install dependencies:
   - `npm install`
3. Run frontend:
   - `node index.js`

Client runs at `http://localhost:5173`

## API endpoints

- `GET /api/students`
- `GET /api/students/:id`
- `POST /api/students`
- `PUT /api/students/:id`
- `DELETE /api/students/:id`
