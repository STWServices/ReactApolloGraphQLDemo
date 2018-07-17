# Signup, Login Into React Native Apps using graphQL, react-apollo with Facebook or Google Logging

## Backend
### Now, let’s set up the backend that handles signup, login using graphQL with mLab database and user authentication via Facebook and Google OAuth apps that we created in the previous steps.

#### These are the tools that we’re going to use:
*	Node.js. A platform that allows JavaScript to be used outside the Web Browsers, for creating web and network applications.
*	Express. Node.js web application framework.
*	Passport. An authentication middleware for Node.js.
*	Passport-Facebook. Facebook authentication strategy for Passport and Node.js.
*	Passport-Google-OAuth20. Google (OAuth 2.0) authentication strategy for Passport.
*	graphql-tools- graphql-tools package are not just useful for building servers. They can also be used in the browser, for example to mock a backend during development or testing
*	express-graphql- The express-graphql module provides a simple way to create an Express server that runs a GraphQL API.
*	Mongoose- Mongoose is a MongoDB object modeling tool designed to work in an asynchronous environment.

#### Initialize Node.js Project
*	Create a new folder called backend:
<img src="Images/mkdir.png" alt="mkdir" width="640" />
Run npm init to create the package.json file, so we can install backend dependencies separately from React Native app:
<img src="Images/npminit.png" alt="npminit" width="640" />
It’s going to ask you a few questions. You can just press return to give the default answers for each question.
*   Install Dependencies
First, install dev dependencies that we’ll going to need during development:
<img src="Images/installDep.png" alt="installDep" width="640" />
And next, install the dependencies that we’ll use to do some work:
<img src="Images/installDep1.png" alt="installDep1" width="640" />
*   Create the Database in mLab
Login in mlab and create new 
<img src="Images/createMlab.png" alt="createMlab" width="640" />


## Demo

<img src="https://github.com/rationalappdev/oauth-login/blob/master/demo.gif" alt="Demo" width="640" />
