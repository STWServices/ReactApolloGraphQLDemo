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

### Installation(after cloning repository run following command from backend path)

```
npm install

```
*	Create the Database in mLab
Login in mlab and create new database 
<img src="Images/createMlab.png" alt="createMlab" width="640" />
<img src="Images/sandbox.png" alt="sandbox" width="640" />
<img src="Images/db_name.png" alt="db_name" width="640" />
<img src="Images/dbCreated.png" alt="dbCreated" width="640" />

#### Put MongoDB URI in server.js mongoose.connect()

#### Launch the Server

Let’s launch the server and see how it works.

*	Open Terminal App and execute:
```
nodemon
```
<img src="Images/nodemon.png" alt="nodemon" width="640" />
That means the server works. That’s great. Keep it running and let’s continue to the mobile app.


## Mobile App
### Now that we have our backend ready let’s build the mobile app with react-apollo.
#### react-apollo - React-Apollo includes a component for providing a client instance to a React component tree, and a higher-order component for retrieving that client instance.
*	Install node-module
```
npm install 
```

### For start project you need to start emulator first , then open Terminal and execute:

```
react-native run-android

```
*	Signup

Result –

<img src="Images/signupcred.png" alt="signupcred" width="200" height="400" />
<img src="Images/signupDb.png" alt="signupDb" width="640" />

*	Login

Result –

<img src="Images/logincred.png" alt="logincred" width="200" height="400" />
If credentials not match it will throw error like below-
<img src="Images/loginUnsuccessful.png" alt="loginUnsuccessful" width="200" height="400" />
For successful login –
<img src="Images/loginDone.png" alt="loginDone" width="200" height="400" />

*	Facebook login 

<img src="Images/fb_start.png" alt="fb_start" width="200" height="400" />
<img src="Images/fb_done.png" alt="fb_done" width="200" height="400" />

*	Google+ login

It will directly call api from server/backend

<img src="Images/gmail_start.png" alt="gmail_start" width="200" height="400" />
<img src="Images/gmail_done.png" alt="gmail_done" width="200" height="400" />

## Facebook Login

#### Setting Up Facebook App
*	Go to https://developers.facebook.com/.
*	Click My Apps and then Add a New App(It will create App ID with App secret)

<img src="Images/addApp.png" alt="addapp" width="640" />

*	Don’t forget to add Email id in Facebook account. 
*	Add platform

Settings ->Basics -> Add platform -> Web

	Set Url , 
	
	e.g https://localhost:4000/auth/facebook/callback
	
<img src="Images/platformAdd.png" alt="platformAdd" width="640" />

*	App Domains(optional)

o	Same as above url - https://localhost:4000/auth/facebook/callback 

*	Privacy Policy URL(optional)	

o	Create policy url here - https://www.freeprivacypolicy.com/

o	After creating policy save that policy with html extension and placed it to Google drive

o	Get sharable link of that file using Right click->Get sharable link from Google drive

o	Place that link to Privacy Policy URL

*	On status 

<img src="Images/statusOn.png" alt="statusOn" width="640" />

*	Add Valid OAuth Redirect URIs  in Facebook Login option(Same as App domain .It is mandatory)

<img src="Images/oauthUrl.png" alt="oauthUrl" width="640" />

*	Save all changes

## Google+ Login

*	Go to https://console.developers.google.com/
*	Click Select a project at the top of the page.
*	Click to create a new project.
*	Enable Google+ API 
*	Create Credentials

<img src="Images/createCred.png" alt="createCred" width="640" />

*	Add credentials for project
<img src="Images/createCred1.png" alt="createCred1" width="640" />
<img src="Images/createCred2.png" alt="createCred2" width="640" />
<img src="Images/createCred3.png" alt="createCred3" width="640" />
<img src="Images/createCred4.png" alt="createCred4" width="640" />
<img src="Images/createCred5.png" alt="createCred5" width="640" />

*	Signing certificate generation

#### If you already having keystore then

```
keytool -exportcert -keystore path-to-debug-or-production-keystore -list –v

```
(“path-to-debug-or-production-keystore” – specify keystore file path)

Note- Run above command from java/bin folder path

otherwise you need to create keystore using following steps:

1) run following command from JDK/bin folder path on command propmt-

2) keytool -genkey -v -keystore D:\my-release-key.keystore -alias my-key-alias -keyalg RSA -keysize 2048 -validity 10000

(“D:\” – you can specify path , here keystore file save in D:\ path)

<img src="Images/createCred6.png" alt="createCred6" width="640" />









	






