# Express.js on Netlify Example

[![Netlify
Status](https://api.netlify.com/api/v1/badges/9aaef7de-1e5d-4fda-bc39-faa10a68b35b/deploy-status)](https://app.netlify.com/sites/netlify-express/deploys)

[![Deploy to
Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/neverendingqs/netlify-express)

An example of how to host an Express.js app on Netlify using
[serverless-http](https://github.com/dougmoscrop/serverless-http). See
[express/server.js](express/server.js) for details, or check it out at
https://netlify-express.netlify.com/!

[index.html](index.html) simply loads html from the Express.js app using
`<object>`, and the app is hosted at `/.netlify/functions/server`. Examples of
how to access the Express.js endpoints:

```sh
curl http://localhost:3000/.netlify/functions/server
curl http://localhost:3000/.netlify/functions/server/another
curl --header "Content-Type: application/json" --request POST --data '{"json":"POST"}' http://localhost:3000/.netlify/functions/server
curl http://localhost:3000/.netlify/functions/server/todos
```

Plese define environment variable for mongoconnection in .env file

MONGO_CLUSTER=<Cluster>
MONGO_PASSWORD=<Password>
MONGO_USER=<User>

on deployed app

App : https://express-demo.netlify.app/.netlify/functions/server/another

https://express-demo.netlify.app/.netlify/functions/server

https://express-demo.netlify.app/.netlify/functions/server/todos
