<h1 align="center">🚀 Challenge #3 - Fixing the code 🚀</h1>

<p align="center">This is the third challenge from <a href="https://www.rocketseat.com.br/ignite">Rocketseat's Ignite</a> Node.js bootcamp.</p>

<p align="center">
  <a href="#about-the-application">About</a> •
  <a href="#technologies">Technologies</a> •
  <a href="#getting-started">Getting Started</a> •
  <a href="#routes">Routes</a> •
  <a href="#running-the-tests">Tests<a>
</p>

<p id="insomnia" align="center">
  <a href="https://insomnia.rest/run/?label=Fix%20Code%20Challenge&uri=https%3A%2F%2Fgithub.com%2Fmarialuizams%2Ffixing-code-challenge-ignite%2Fblob%2Fmain%2Finsomnia.json" target="_blank"><img src="https://insomnia.rest/images/run.svg" alt="Run in Insomnia"></a>
</p>

## About the application

This application performs the CRUD operations of projects repositories. In addition, it is possible to like registered repositories, increasing the number of likes by 1 each time the route is called.

The repository structure must be as shown below:

```
{
  id: uuid(),
  title,
  url,
  techs,
  likes: 0
}
```
Where:

- **id** must be a valid uuid;
- **title** is the title of the repository (ex: unform);
- **url** is the repository url (ex: https://github.com/unform/unform);
- **techs** is an array where each element must be a string with the name of the technology related to the repository (ex: ["react", "react-native", "form"]);
- **likes** is the number of likes the repository has received.

Note that the number of likes must always be zero when a repository is created.

## Technologies

- [Node.js](https://nodejs.org/en/)
- [Express](http://expressjs.com/)
- [Jest](https://jestjs.io/)

## Getting Started

Clone this repository and access the folder:
```
$ git clone https://github.com/marialuizams/fixing-code-challenge-ignite
$ cd fixing-code-challenge-ignite
```
Install dependencies using:
```
$ yarn
# or
$ npm install
```

Start the app by running:
```
$ yarn dev
```
The application should start running on http://localhost:3333.

Import the `insomnia.json` file on the Insomnia app, or click the [Run in Insomnia](#insomnia) button.

## Routes

### POST `/repositories`

This route should receive `title`, `url` and `techs` via request body:

```json
{
  "title": "api",
  "url": "https://github.com/user/api",
  "techs": ["nodejs", "express"]
}
```
And return an object with the repository info and a `201` status code.

```json
{
  "id": "uuid",
  "title": "api",
  "url": "https://github.com/user/api",
  "techs": ["nodejs", "express"],
  "likes": 0
}
```
### GET `/repositories`

This route should return a list of all the registered repositories.

### PUT `/repositories/:id`

This route should receive `title`, `url` and `techs` through the request body and the repository's `id` that must be received as a route parameter. This method should change only the information received by the request body.

### DELETE `repositories/:id`

This route should receive the `id` of the repository as a route parameter and return the repository with the updated number of likes.

## Running the tests
To run the tests using Jest:
```
$ yarn test
```

![Jest output](/assets/test_evidence.png)

#

<p align="center">Developed by <a href="https://www.linkedin.com/in/marialuizasalviano/">Maria Luiza Salviano</a></p>