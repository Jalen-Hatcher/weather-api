# Overview
A backend, RESTFul api which serves (hypothetical) weather data from a remote, MongoDb database. 

# Request Formatting
All data communicated from some endpoint to the server is in JSON format. In this application, appropriate descriptions related to weather will be sent via the following schema: <br />
{<br />
  &ensp;date: Date,<br />
  &ensp;city: String,<br />
  &ensp;state: String,<br /> 
  &ensp;country: String,<br />
  &ensp;temperature: Number,<br />
  &ensp;condition: String<br />
}<br />
Additionally, _id and __v attributes will be sent indicating entry id and version keys respectively for the database entries. Data can be requested via the HTTP route localhost:PORT/id, where id represents the _id attribute for a specific entry.

# Note on .env
The src/server.js file will not connect to a MongoDb database without a connection string defined in an external .env file. For protection purposes, this file has not been supplied so the user is expected to provide a valid MongoDb connection string
