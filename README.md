# Flask server

## Summary
This app is a simple server with a single endpoint '/placesAndGifs.json'.

It takes a POST request with Content-Type: application/json. In the request body it expects a key 'query' to point to a string value. Using that string, the server will retrieve a number of locations from the Google Places API text search endpoint.

After retrieving those, it will use place's name to grab gif objects from the Giphy API's search endpoint. All those results are associated with the Google results having the key 'giphies'.

This resulting object is dumped into a json file and sent back to the client or requester.

This project may be hosted on Heroku for a time and can be queried using the following cURL command:

curl -H "Content-Type: application/json" -X POST -d '{"query":"\<Your Query Here\>"}' -O https://maps-giphy-2.herokuapp.com/placesAndGifs.json

If leaving out the -O, using Postman, etc., the data should comeback as a JSON object.

## Issues

If there any issues, please feel free to raise an issue or email me. Email can be found on GitHub - **_@andrewzheng8_**.
