# Restfull-APITesting-Collection
My first API Testing Project in POSTMAN / All operations have been carried out CRUD ( Create, Read, Update, Delete )
## About the project 
The project was carried out with the help of those from https://restful-booker.herokuapp.com who also provided me with the necessary documentation for API testing.
## Create Environments 
We have achieved 3 environments to make our work easier. 

1. "env" - It was created to contain our endpoint https://restful-booker.herokuapp.com 
2. "token" - It was created to contain the authorization token 
3. "bookingid" - It was created to contain the ID of the desired book 

<img width="600" alt="Screenshot 2022-08-24 at 16 43 05" src="https://user-images.githubusercontent.com/34375010/186434913-b5b58503-d493-40f1-922e-125f70005b94.png">

## Use of Snippets 
We used different snippets to automate the testing process.

## CRUD Operations

1. GET Ping Server

:triangular_flag_on_post: Environments 

``` 
pm.test("Created", function () {
    pm.expect(pm.response.text()).to.include("Created");
}); 

``` 
This environment was created to test whether it comes as a "created" response.

<img width="600" alt="Screenshot 2022-08-24 at 17 04 34" src="https://user-images.githubusercontent.com/34375010/186439217-f36dd0c6-1158-4394-908d-fade55428411.png">
