GitHubAPIs_TestSample

1. This POSTMAN project tests sample GitHub account and uses REST API documented at https://docs.github.com/en/rest?apiVersion=2022-11-28  
   I mainly used requests relating to repositories. Please see https://docs.github.com/en/rest/repos/repos?apiVersion=2022-11-28 for reference.

2. Project description:
   Projekt is designed to test possibility of creating a new repository for current user, then its reading, update and finally deletion.
   It uses basic CRUD methods: POST, READ, PUT(PATCH), DELETE and OAuth2 authorization which is stored in 'Token' variable, available for whole Colletion.
   Variables 'Token', 'User' and 'url' are defined in 'GitHub Environment'.
   Collection variable ('NewRepo') stores the name of newly created repo and is used in further requests for its reading, update and deletion.

   'Get authenticated user' request is run first in order to obtain login (user).
   Test included in this request cheks its status code (200) and sets environmental variable 'User' to be the current user from the response body.
   After creating a new repo or its update, collection varaible 'NewRepo' gets refreshed.

   Data are pased to the reqests from Environment or Collection variables. Those are updated using scripts inside tests. 

3. The purpose of this simple 'end-to-end' project is to present some basic POSTMAN REST API testing skills that I acquired during my 
   online tutorial self-studying. 

4. Scope of knowledge:
   - Creating collections, environments, requests, basic tests and scripts.
   - Using 'Collection Runner'
   - Creating and accessing variables at different levels (inside body, endpoints, tests, collections, environments)
   - Creating simple scripts:
     > Passing data between requests and accessing variables at different leves.
     > Creating simple tests
     > Console logging
     > Creating simple assertions
     
Please note that the initial token currently set in 'GitHub Environment' is not valid.
Internal GitHub scanner deactivated it as soon as this project was pushed into github repo.
I'll be happy to provide a valid token once the recruiting person is interested to run this project.
After updating 'Token' variable inside 'GitHub Environment' all works fine.
Token scope on GitHub is set in a way that doesn't disclose any sensitive data anyway.


      