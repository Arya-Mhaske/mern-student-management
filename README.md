# Minimal MERN Student App

## Structure

- `server` - Node.js, Express, MongoDB (Mongoose), Student CRUD API
- `client` - React (Vite), Axios UI for add/list/delete students

## Initial Setup

clone the repository by
git clone repo_url

# update packages
sudo apt update
DO NOT sudo apt install node as it will install an older version of node incompatible with vite

## IMPORTANT! Install Node Version Manager first (NVM) and use it to install Node Version 20.x.x
1. curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
2. nvm install 22
3. nvm use 22

## AZURE INBOUND RULES
under the instance's networking (firewall) settings, allow the following port configurations to accept traffic from all IP's

{
port: 5173
protocol: any
source: any
destination: any
}

{
port: 5000
protocol: any
source: any
destination: any
}

5173: frontend
5000: server

you can find this on your azure account.

## Backend setup

1. Go to `server`
2. Install dependencies:
   - `npm install`
3. Create `.env` and paste your credentials
   the .env shall contain two things
   {
   PORT=5000
   MONGO_URI=<connection_string>
   }
5. Run server:
   - `node index.js`

Server runs at `http://localhost:5000`

## Frontend setup

# !IMPORTANT PREREQUISITE
right now the frontend might not be able to talk to backend server because frontend API requests use localhost:5000. your machine does not understand localhost. use the public IP of the instance instead. where would you change this configuration?

check in /client/src/App.jsx
edit the App.jsx file and update the 

API_BASE_URL to "http:<public_ip>:SERVER_PORT(5000)/api/students"
and save.
now your frontend should be configured to talkto your backend server.

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
