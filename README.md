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
