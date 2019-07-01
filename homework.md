1. What is responsible for defining the routes of the `games` resource?

  The create_router file in the server folder specifies the restful routes template. The server.js file then creates gamesRouter using the template and the url address ‘/api/games’, passing it gamesCollection as the data.  

2. What do you notice about the folder structure?  

Whats the client responsible for?

  The client deals with the rendering of information gained from the database/api/seeds file to the browser; views & components; user input forms; CSS styling, etc. - the ‘front-end’.

Whats the server responsible for?

  The server deals with the routes and the database - the ‘back-end’.

3. What are the responsibilities of server.js?

  “The express server (server.js) listens for requests being made to the routes it has defined”. It also connects with the database. It requires the necessary bits to enable the data to be accessed from anywhere (no ‘cors’ errors).

4. What are the responsibilities of the `gamesRouter`?

  The gamesRouter sets up restful routes according to the create_router file. This enables CRUD functionality with the data in the database.

5. What process does the client (front-end) use to communicate with the server?

  It fetches the json data from the url in GamesService.js by sending and receiving requests/responses. I.e. ‘getGames’, ‘postGame’ & ‘deleteGame’.

6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs

  Fetch defaults to ‘get’ method. When requesting a route other than ‘get’ fetch has an additional parameter in the form of an object containing the method type; body & headers.

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?

  ‘Get’, ‘post’ & ‘delete’.

8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?

  To store & seed our games data.

EXTENSION: Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

  To be able to delete by id - a unique marker rather than an index which can change.
