# Movie Review App

* MERN stack: A Movie Review App
* Backend at root, frontend at a separate folder
* Use proxy to backend /api and /auth for development
* Local and Social Login/Signup
* Users can browse movies [API from The Movie Database (TMDb)], write reviews, and follow others' reviews.

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
### If run MongoDB locally

#### Install MongoDB
#### Make a local storage: say d:/mongodb/data
#### Open one cmd/terminal (1st terminal)
```
"C:\Program Files\MongoDB\Server\3.6\bin\mongod.exe" --dbpath="d:\mongodb\data"
```
#### Need to see this: [initandlisten] waiting for connections on port 27017

#### Connect to MongoDB: open ANOTHER cmd/terminal (2nd terminal)
```
"C:\Program Files\MongoDB\Server\3.6\bin\mongo.exe"
```
## Clone git repo
```
git clone https://github.com/duongch4/mern-project-dev
```
## At root level, i.e. backend part
### Create a file named ".env" on the same level as "server.js":
```
PORT=5000
MONGODB_URI=mongodb://localhost:27017/<Supply your db name>
GITHUB_CLIENT_ID=<Supply dummy string if does not have>
GITHUB_CLIENT_SECRET=<Supply dummy string if does not have>
GITHUB_CALLBACK=http://localhost:3000/auth/github/callback
FACEBOOK_CLIENT_ID=<Supply dummy string if does not have>
FACEBOOK_CLIENT_SECRET=<Supply dummy string if does not have>
FACEBOOK_CALLBACK=http://127.0.0.1:3000/auth/facebook/callback
GOOGLE_CLIENT_ID=<Supply dummy string if does not have>
GOOGLE_CLIENT_SECRET=<Supply dummy string if does not have>
GOOGLE_CALLBACK=http://127.0.0.1:3000/auth/google/callback
```
### Open a terminal/cmd for backend (3rd ternminal)
### Install dependencies
```
npm install
```
### Run: for development
```
npm run start-dev
```
### Should see
```
API running on port 5000
MongoDB is connected
```

## Go to frontend folder
### Open another terminal/cmd for frontend (4th terminal)
### Install dependencies
```
npm install
```
### Run
```
npm start
```
Should open a browser automatically on http://localhost:3000

### In frontend/package.json
#### For development
```
  "proxy": {
    "/auth": {
      "target": "http://localhost:5000"
    },
    "/api": {
      "target": "http://localhost:5000"
    }
  }

```
#### For deployment: Heroku
```
  "proxy": "http://localhost:5000"
```
