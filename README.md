# mern-passport-dev

* MERN stack
* Divide backend and frontend separately, and use proxy to backend /api and /auth for development

# Some of the techs used:

## Frontend
* React: create-react-app
* Redux
* React router v4
* Bootstrap v4
* Webpack 4
* Jest
* SCSS
* development: proxy backend /api and /auth

## Backend
* MongoDB
* Express
* NodeJS
* Passport: Local & Social (Github, Google, Facebook)
* Bcryptjs

# Getting started

## Hook up a MongoDB: either locally or remotely

## Go to backend folder
### Create .env file on the same level as server.js:
```
PORT=5000
MONGODB_URI=mongodb://localhost:27017/
GITHUB_CLIENT_ID=<Supply dummy string if does not have>
GITHUB_CLIENT_SECRET=<Supply dummy string if does not have>
GITHUB_CALLBACK=http://127.0.0.1:3000/auth/github/callback
FACEBOOK_CLIENT_ID=<Supply dummy string if does not have>
FACEBOOK_CLIENT_SECRET=<Supply dummy string if does not have>
FACEBOOK_CALLBACK=http://127.0.0.1:3000/auth/facebook/callback
GOOGLE_CLIENT_ID=<Supply dummy string if does not have>
GOOGLE_CLIENT_SECRET=<Supply dummy string if does not have>
GOOGLE_CALLBACK=http://127.0.0.1:3000/auth/google/callback
```
### Open a terminal/cmd for backend
### Install dependencies
```
npm install
```
### Run
```
npm start
```
### Should see
```
API running on port 5000
MongoDB is connected
```

## Go to frontend folder
### Open a terminal/cmd for frontend
### Install dependencies
```
npm install
```
### Run
```
npm start
```
Should open a browser automatically on http://localhost:3000

