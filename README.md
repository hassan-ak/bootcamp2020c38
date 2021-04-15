# bootcamp2020c38
- JAM-Stack

## Step22 Gatsby Netlify Functions Apollo Server Lambda Helloworld
External Links:-
- [Deploying a GraphQL API on Netlify serverless functions with apollo-server-lambda](https://egghead.io/lessons/apollo-deploying-a-graphql-api-on-netlify-serverless-functions-with-apollo-server-lambda)
- [Deploying with Netlify Functions](https://www.apollographql.com/docs/apollo-server/deployment/netlify/)
- [Deploy a fullstack Apollo app with Netlify](https://www.apollographql.com/blog/deploy-a-fullstack-apollo-app-with-netlify-45a7dfd51b0b/)
- [Demo of combining build-time Gatsby queries with client-side Apollo queries.](https://github.com/jlengstorf/gatsby-with-apollo)
- [wrapRootElement API](https://www.gatsbyjs.com/docs/browser-apis/#wrapRootElement)

Steps:-
- we will add a dependency package in the netlify function
  - cd functions/graphql_hello
  - npm init
  - npm install --save apollo-server-lambda graphql
  - add graphql_hello.js hello world code
- netlify dev
- Note that there are three servers running on local host, Functions server is listening on port 52810, Gatsby server running on port 8000, and proxy server running at port 8888
- GraphQL Playgroud 
  - http://localhost:8888/.netlify/functions/graphql_hello
- Now lets start building the client:
  - npm install @apollo/client --save
  - [Demo of combining build-time Gatsby queries with client-side Apollo queries.](https://github.com/jlengstorf/gatsby-with-apollo)
  - We will only use the client-side Apollo queries in this step
  - [wrapRootElement API](https://www.gatsbyjs.com/docs/browser-apis/#wrapRootElement)
- Open in the Browser: http://localhost:8888
- Now lets publish the project on Netlify:
- We have to change the URL in the src/apollo/client.js file
- Create a netlify.toml file with publish directory public and build command
- yarn build
- Login to Netlify on Local Machine to start the publishing process (not required if you have already logged in in step 13):
  - netlify login
- To publish on Netlify:
  - netlify deploy --prod
- Notice that the tool has created .netlify directory in your project folder.
- Now the site is published and you can copy the link given by the tool in the browser.
- Add /.netlify in .gitignore before pushing to public repo

## Step23 Gatsby Netlify Functions Apollo Server Lambda Faunadb
External Links:-
- [Deploying a GraphQL API on Netlify serverless functions with apollo-server-lambda](https://egghead.io/lessons/apollo-deploying-a-graphql-api-on-netlify-serverless-functions-with-apollo-server-lambda)
- [Deploying with Netlify Functions](https://www.apollographql.com/docs/apollo-server/deployment/netlify/)
- [Deploy a fullstack Apollo app with Netlify](https://www.apollographql.com/blog/deploy-a-fullstack-apollo-app-with-netlify-45a7dfd51b0b/)
- [Demo of combining build-time Gatsby queries with client-side Apollo queries.](https://github.com/jlengstorf/gatsby-with-apollo)
- [wrapRootElement API](https://www.gatsbyjs.com/docs/browser-apis/#wrapRootElement)

Steps:-
- Now we will add a dependency package in the netlify function
  - cd functions/graphql_faunadb
    - npm init
    - npm install --save apollo-server-lambda graphql
    - add graphql_faunadb.js code
- Note that the resolver is async so that we can use await the faunadb query
- netlify dev
- Note that there are three servers running on local host, Functions server is listening on port 52810, Gatsby server running on port 8000, and proxy server running at port 8888
- GraphQL Playgroud 
  - http://localhost:8888/.netlify/functions/graphql_faunadb
- Now lets start building the client which will be same as in last steps code:
  - npm install @apollo/client --save
  - [Demo of combining build-time Gatsby queries with client-side Apollo queries.](https://github.com/jlengstorf/gatsby-with-apollo)
- We will only use the client-side Apollo queries in this step
  - [wrapRootElement API](https://www.gatsbyjs.com/docs/browser-apis/#wrapRootElement)
- Open in the Browser:
  - http://localhost:8888
- Now lets publish the project on Netlify:
  - We have to change the URL in the src/apollo/client.js file
  - Create a netlify.toml file with publish directory public and build command
  - yarn build
- Login to Netlify on Local Machine to start the publishing process (not required if you have already logged in in step 13):
  - netlify login
- To publish on Netlify:
  - netlify deploy --prod
- Notice that the tool has created .netlify directory in your project folder.
- Now the site is published and you can copy the link given by the tool in the browser.
- Add /.netlify in .gitignore before pushing to public repo

## Step24 Gatsby Netlify Contentful Auto Build
- This Step is covered in Bootcamp2020c31

External Links
- [Guid to integrate git repo with netlify to auto build on commit](https://www.netlify.com/blog/2016/09/29/a-step-by-step-guide-deploying-on-netlify/)
- [Trigger netlify build on changes in contentful](https://www.contentful.com/developers/docs/tutorials/general/automate-site-builds-with-webhooks) 
- [Deployed URL](https://quizzical-shannon-7cc5d5.netlify.app/)

Gatsby Blog Site
- Blog Site in Gatsby with dynamic page generation of each post on build time. Integrated with netlify and auto build on commit plus integrated with contentful so as changes will be published in contentful it will trigger build on netlify

## Step25 Mongodb Mongoose Crud Node
- Mongodb Database with Mongoose library, Setup a Collection, and Create an Index with Node.js

External Links:-
- [What is Mongodb](https://docs.mongodb.com/manual/introduction/)
- [Mongoose](https://mongoosejs.com/)
- [Mongoose Quick Start](https://mongoosejs.com/docs/index.html)
- [Introduction to Mongoose for MongoDB](https://www.freecodecamp.org/news/introduction-to-mongoose-for-mongodb-d2a7aa593c57/)
- [Using a Database with Mongoose](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/mongoose)
- [What is MongoDB Atlas](https://www.mongodb.com/cloud/atlas/efficiency)
- [Introducing MongoDB Atlas](https://www.mongodb.com/presentations/introducing-mongodb-atlas)
- [Get Started with Atlas](https://docs.atlas.mongodb.com/getting-started/)
- [Set Up a Free Tier MongoDB Atlas Cluster](https://studio3t.com/knowledge-base/articles/mongodb-atlas-tutorial/)
- [Signup for Mongodb Atlas Service](https://www.mongodb.com/cloud/atlas/signup)
- [Install DotEnv](https://www.npmjs.com/package/dotenv)
- [article](https://studio3t.com/knowledge-base/articles/mongodb-atlas-tutorial/)

Steps to Follow:-
- [Signup for Mongodb Atlas Service](https://www.mongodb.com/cloud/atlas/signup)
- Create a Project Directory
  - npm init
  - [Install DotEnv](https://www.npmjs.com/package/dotenv)
  - npm install dotenv --save
  - npm install mongoose --save
- Go to [article](https://studio3t.com/knowledge-base/articles/mongodb-atlas-tutorial/) and see how to create database and get connection string and then paste connection string in .env file with the name MONGODB_CONNECTION_STRING=my-db-connection-string
- Write and Run Node Programs:
  - node step00-database-connection
  - Do the same with all steps

Topics Covered:-
- Database connection
- create schema add document
- Create schema with index
- Create multiple documents
- Fetch all documents
- Find by field
- Find by id
- Find single document
- Find and update document
- Update one document
- Update many document
- FindById and update
- Findone and update
- Replace document
- Delete document
- Delete many documents
- FindById and delete
- Related document one to one
- Populate related documents
- Related document one to many
- Related document one to many2

## Step26 Gatsby Netlify Functions Mongodb
External Links:-
- [Using Netlify Functions with Gatsby](https://joshwcomeau.com/gatsby/using-netlify-functions-with-gatsby/)
- [Netlify Dev](https://www.netlify.com/products/dev/)
- [Using Mongoose With AWS Lambda](https://mongoosejs.com/docs/lambda.html)
- [Mongodb -- Best Practices Connecting from AWS Lambda](https://docs.atlas.mongodb.com/best-practices-connecting-to-aws-lambda/)
- [Things you should know before connecting your AWS Lambda function to a database](https://medium.com/javascript-in-plain-english/serverless-things-i-wish-i-had-known-part-2-dynamodb-x-mongodb-x-aurora-serverless-1053cfddff36)
- [Manage RDS Connections from AWS Lambda Serverless Functions](https://www.jeremydaly.com/manage-rds-connections-aws-lambda/)

Steps:- 
- Now we will add a dependency package in the netlify function
  - cd functions/hello
  - npm init
  - npm i --save mongoose
- Update hello.js code and call to MongoDB
- Environment Variables
  - If the current project is linked to a Netlify site (netlify link), environment variables are pulled down from production and populated in netlify dev server. This functionality requires that you're logged in (netlify login) and connected to the internet when running netlify dev.
  - Netlify Dev also supports local environment variables through .env files. Netlify Dev will look in project root directory for .env file and will provide those variables to the spawned site generator/server and Netlify Functions.
  - For local function development you will create .env file at the root directory with the following entry:
    - MONGODB_CONNECTION_STRING=my-db-connection-string
- add .env in .gitignore
- Add useEffect hook in index.tsx
- netlify dev
  - Note that there are three servers running on local host, Functions server is listening on port 52810, Gatsby server running on port 8000, and proxy server running at port 8888
  - Open in the Browser: http://localhost:8888
- Create a netlify.toml file with publish directory public and build command
  - Now set the envirnoment variables i.e. MONGODB_CONNECTION_STRING in the netlify.toml file
- We have implemented the first option mentioned here: https://docs.netlify.com/configure-builds/environment-variables/#declare-variables
- yarn build
- Login to Netlify on Local Machine to start the publishing process (not required if you have already logged in in step 13):
  - netlify login
- To publish on Netlify:
  - netlify deploy --prod
- Notice that the tool has created .netlify directory in your project folder.
- Now the site is published and you can copy the link given by the tool in the browser.
- Add /.netlify in .gitignore before pushing to public repo

## Step27 Gatsby Netlify Functions Mongodb Formik
External Links:-
- [Netlify Functions Examples](https://functions-playground.netlify.app/)
- [Advanced Examples](https://functions.netlify.com/examples/)
- [Using Mongoose With AWS Lambda](https://mongoosejs.com/docs/lambda.html)
- [Mongodb -- Best Practices Connecting from AWS Lambda](https://docs.atlas.mongodb.com/best-practices-connecting-to-aws-lambda/)
- [Things you should know before connecting your AWS Lambda function to a database](https://medium.com/javascript-in-plain-english/serverless-things-i-wish-i-had-known-part-2-dynamodb-x-mongodb-x-aurora-serverless-1053cfddff36)
- [Manage RDS Connections from AWS Lambda Serverless Functions](https://www.jeremydaly.com/manage-rds-connections-aws-lambda/)

Steps:-
- Now we will add a dependency package in the netlify function
  - cd functions/add
  - npm init
  - npm i --save mongoose
  - Add add.js code and call to MongoDB
- Environment Variables
  - If the current project is linked to a Netlify site (netlify link), environment variables are pulled down from production and populated in netlify dev server. This functionality requires that you're logged in (netlify login) and connected to the internet when running netlify dev.
  - Netlify Dev also supports local environment variables through .env files. Netlify Dev will look in project root directory for .env file and will provide those variables to the spawned site generator/server and Netlify Functions.
  - For local function development you will create .env file at the root directory with the following entry:
    - MONGODB_CONNECTION_STRING=my-db-connection-string
- add .env in .gitignore
- Add Form in index.tsx
- netlify dev
- Note that there are three servers running on local host, Functions server is listening on port 52810, Gatsby server running on port 8000, and proxy server running at port 8888
- Open in the Browser: http://localhost:8888
- Create a netlify.toml file with publish directory public and build command
  - Now set the envirnoment variables i.e. MONGODB_CONNECTION_STRING in the netlify.toml file
- We have implemented the first option mentioned here: https://docs.netlify.com/configure-builds/environment-variables/#declare-variables
- yarn build
- Login to Netlify on Local Machine to start the publishing process (not required if you have already logged in in step 13):
  - netlify login
- To publish on Netlify:
  - netlify deploy --prod
  - Notice that the tool has created .netlify directory in your project folder.
- Now the site is published and you can copy the link given by the tool in the browser.
- Add /.netlify in .gitignore before pushing to public repo
