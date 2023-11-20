This is the documentation for good-chatbot, completed as a project for goodspace.
- Github link: https://github.com/TanishqSingla/goodchatbot
- Deployment link: https://goodchatbot-production.up.railway.app/

## Overview of the project
The project uses openai to reply to prompts. The technologies used to build this project are
- Node.js
- Socket.io
- Express.js
- MongoDB
- openai
- EJS

## Docs
Following is the doc explaining different parts of the project.
#### server.js
This file is the entry-point of the application, here we initialize our middlewares, socket and db connections. 

**Environments**
`server.js` file supports multiple modes, some of the defaults include
- production
- development
The mode is initialized in the scripts, mentioned in `package.json` in the NODE_ENV environment variable. Using this environment variable respective env file is loaded in the program.

#### app.js
`app.js` initializes the express framework, here we also define our middlewares in an orderly manner. 
Here we are using the following middlewares
- `view engine` - EJS is used as view engine to render html pages to user.
- `express.json()` - To parse requests which have `Content-Type` as `application/json`. This parses the payload and add the objects in the `Request.body` object of express.
- `router` - This is our router, this middleware is used to redirect user to different resources our backend application supports.
- `errorHandler` - This middleware is used to capture any unexpected error thrown in the middleware so we can send an appropriate response to the user.

#### models
`models` folder contain our mongodb models. Here the chat model is defined with the following properties.
Chat
> user: String
> message: String
> timestamps: Date

#### public
`public` folder contains our static files such as scripts and styles that are sent to frontend.

#### services
Services folder contain files denoting any third party service that the app is using. In our case its the openai service that we're using.

#### views
Views folder contains our templates that are going to be used by ejs view engine.

#### router
router contains our express router middleware, which I am using to route user query to different functions.

## Flow of app
![[Screenshot from 2023-11-20 23-35-23.png]]