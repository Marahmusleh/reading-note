## Status Codes Based On REST Methods:
1. In your own words, describe what each group of status code represents:
* 100’s =telling the client that its request will fail before they start sending the body 200’s = telling the client that its request was accepted 300’s = telling the client that the resource they are requesting isn’t available 400’s = invalid requests a client sent to a server 500’s = unreachable servers

2. What is a status code 202?
* Used for asynchronous processing. This code tells the client that the request was valid, but its processing will finish sometime in the future.(1)

3. What is a status code 308?
* This tells the client to use another URL to access the resource and not use the current URL anymore.(1)

4. What code would you use if an update didn’t return data to a client?
* 204 code

5. What code would you use if a resource used to exist but no longer does?
* 410 code

6. What is the ‘Forbidden’ status code?
* 403 code

## Build A REST API With Node.js, Express & MongoDB (Video):
1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
* To deploy our application.

2. What is middleware?
* Code that runs once the server got the request but before passed to the route

3. What does app.use(express.json()) do?
* Let our server accept json as a body inside a post element or get element ...etc

4. What does the /:id mean in a route?
* This means its parameter and used to get all parameters passed after the slash

5. What is the difference beween PUT and PATCH?
* PUT update all info (replace info), PATCH update only specific item (modify).

6. How do you make a defalut value in a schema?
* inside schema value add default: THE VALUE YOU WANT TO BE DEFAULT

7. What does a 500 error status code mean?
* There is error on server

8. What is the difference between a status 200 and a status 201?
* 201 says specifically that you created something, but 200 says success only (201 code used in post request)
