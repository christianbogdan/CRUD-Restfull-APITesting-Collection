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

:triangular_flag_on_post: Snippets 

``` 
pm.test("Created", function () {
    pm.expect(pm.response.text()).to.include("Created");
}); 

``` 
This snippet was created to test whether it comes as a "created" response.

<img width="600" alt="Screenshot 2022-08-24 at 17 04 34" src="https://user-images.githubusercontent.com/34375010/186439217-f36dd0c6-1158-4394-908d-fade55428411.png">

2. POST Auth 

:triangular_flag_on_post: Snippets  

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain token", function () {
    pm.expect(pm.response.text()).to.include("token");
});
var jsonData = JSON.parse(responseBody);
postman.setEnvironmentVariable("token", jsonData.token);
pm.globals.set("token", jsonData.token )
``` 
This snippet was created to check status 200 if the answer received contains the word "token".

<img width="600" alt="Screenshot 2022-08-24 at 17 12 53" src="https://user-images.githubusercontent.com/34375010/186441244-db9fa236-b06b-44ba-a378-24266d877cf3.png">

3. Auth without Username&Password 

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials".

<img width="600" alt="Screenshot 2022-08-24 at 17 17 00" src="https://user-images.githubusercontent.com/34375010/186442152-df6cf4b8-a93d-4741-b121-a8d86cd72054.png">

<img width="600" alt="Screenshot 2022-08-24 at 17 18 26" src="https://user-images.githubusercontent.com/34375010/186442462-85c28c41-b595-483b-8b82-80eb3c325b86.png">

4. Auth without Password 

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials".

<img width="600" alt="Screenshot 2022-08-24 at 17 22 21" src="https://user-images.githubusercontent.com/34375010/186443318-0df51198-fc8c-4f73-a197-98eca3e8c655.png">
<img width="600" alt="Screenshot 2022-08-24 at 17 23 04" src="https://user-images.githubusercontent.com/34375010/186443502-417cdb38-cec6-4bf7-87a4-f0298faaa747.png">


5. Auth without Username 

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials".

<img width="600" alt="Screenshot 2022-08-24 at 17 22 21" src="https://user-images.githubusercontent.com/34375010/186443318-0df51198-fc8c-4f73-a197-98eca3e8c655.png">

6. Auth with blank password

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials".

<img width="600" alt="Screenshot 2022-08-24 at 17 26 26" src="https://user-images.githubusercontent.com/34375010/186444217-1f811dcd-2144-4730-b5ac-e45c18da2316.png">

7. Auth with blank username

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials".

<img width="600" alt="Screenshot 2022-08-24 at 17 27 49" src="https://user-images.githubusercontent.com/34375010/186444554-4cc47352-88c9-41bd-ba8e-72b6472d117a.png">

8. Auth with wrong Username&Password

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials".

<img width="600" alt="Screenshot 2022-08-24 at 17 29 08" src="https://user-images.githubusercontent.com/34375010/186444955-b9f3bcc7-1fd4-484f-8740-d4b2e57140ef.png">


9. Auth with wrong Username

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials".

<img width="600" alt="Screenshot 2022-08-24 at 17 36 27" src="https://user-images.githubusercontent.com/34375010/186446677-71bda02d-d84a-48f9-9b2d-1c48e4380b6c.png">

10. Auth with wrong Password

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials". 

<img width="600" alt="Screenshot 2022-08-24 at 17 33 51" src="https://user-images.githubusercontent.com/34375010/186446072-58d9ac26-e422-4baf-88f8-63b1c1b3d92f.png">

11. Create new booking 

:triangular_flag_on_post: Snippets 

<details><summary> Click to expand code </summary>

 ```
 pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Body contain bookingid", function () {
    pm.expect(pm.response.text()).to.include("bookingid");
});

pm.test("Body contain firstname", function () {
    pm.expect(pm.response.text()).to.include("firstname");
});

pm.test("Body contain Cristian", function () {
    pm.expect(pm.response.text()).to.include("Cristian");
});

pm.test("Body contain lastname", function () {
    pm.expect(pm.response.text()).to.include("lastname");
});

pm.test("Body contain Cristian", function () {
    pm.expect(pm.response.text()).to.include("Cristian");
});

pm.test("Body contain totalprice", function () {
    pm.expect(pm.response.text()).to.include("totalprice");
});

pm.test("Body contain 150", function () {
    pm.expect(pm.response.text()).to.include("150");
});

pm.test("Body contain depositpaid", function () {
    pm.expect(pm.response.text()).to.include("depositpaid");
});

pm.test("Body contain false", function () {
    pm.expect(pm.response.text()).to.include("false");
});

pm.test("Body contain bookingdates", function () {
    pm.expect(pm.response.text()).to.include("bookingdates");
});

pm.test("Body contain checkin", function () {
    pm.expect(pm.response.text()).to.include("checkin");
});

pm.test("Body contain checkout", function () {
    pm.expect(pm.response.text()).to.include("checkout");
});

pm.test("Body contain additionalneeds", function () {
    pm.expect(pm.response.text()).to.include("additionalneeds");
});

var jsonData = JSON.parse(responseBody);
pm.globals.set("bookingid", jsonData.bookingid)

 ```
</details>


This snippet was created to check the status of 200 if the answer received contains the following: Bookingid, firstname, Cristian, lastname, Cristian, totalprice, 150, depositpaid, false, bookingdates, checkin, checkout, addtionalneeds. 

<img width="600" alt="Screenshot 2022-08-24 at 17 43 26" src="https://user-images.githubusercontent.com/34375010/186448381-5e604404-98a8-409f-a7f8-0c0036706ab7.png"> 
   

12. View booking without First Name 

:triangular_flag_on_post: Snippets

```
pm.test("Status code is 500", function () {
    pm.response.to.have.status(500);
});
pm.test("Body contain Internal Server Error", function () {
    pm.expect(pm.response.text()).to.include("Internal Server Error");
});

```
This snippet was created to check the status of 500 if the answer received contains "Internal Server Error". 

<img width="600" alt="Screenshot 2022-08-24 at 19 02 10" src="https://user-images.githubusercontent.com/34375010/186466888-b84168c0-9539-4eb3-a57a-451d1706dedf.png">

13. View all booking 
 
:triangular_flag_on_post: Snippets 

```
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Body contain bookingid", function () {
    pm.expect(pm.response.text()).to.include("bookingid");
});

```
This snippet was designed to check the status of 200 and to have "bookingid" in the body.

<img width="600" alt="Screenshot 2022-08-24 at 19 05 10" src="https://user-images.githubusercontent.com/34375010/186467759-5a633f69-61a8-445f-ae33-707b6950af2a.png">

14.View all booking with Michael First Name 

:triangular_flag_on_post: Snippets 

```
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Body contain bookingid", function () {
    pm.expect(pm.response.text()).to.include("bookingid");
});

```
This snippet was designed to check the status of 200 and to have "bookingid" in the body.

<img width="600" alt="Screenshot 2022-08-25 at 12 21 19" src="https://user-images.githubusercontent.com/34375010/186627383-078c65c3-e937-4a45-acfb-9957b0f77db1.png">


15.View all booking with wrong First Name

:triangular_flag_on_post: Snippets 

```
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Body contains an empty list []", function () {
    pm.expect(pm.response.text()).to.include("[]");
});
```

This snippet was created to check the status is 200 and to have "[]" in the body. 

<img width="600" alt="Screenshot 2022-08-25 at 12 26 02" src="https://user-images.githubusercontent.com/34375010/186630773-e0d9eec2-f680-4e60-937d-04cdf8ae3610.png">

16.GET Booking after ID

:triangular_flag_on_post: Snippets

<details><summary> Click to expand code </summary>

```
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});


pm.test("Body contains firstname", function () {
    pm.expect(pm.response.text()).to.include("firstname");
});
pm.test("Body contains lastname", function () {
    pm.expect(pm.response.text()).to.include("lastname");
});
pm.test("Body contains totalprice", function () {
    pm.expect(pm.response.text()).to.include("totalprice");
});
pm.test("Body contains depositpaid", function () {
    pm.expect(pm.response.text()).to.include("depositpaid");
});
pm.test("Body contains bookingdates", function () {
    pm.expect(pm.response.text()).to.include("bookingdates");
});
pm.test("Body contains checkin", function () {
    pm.expect(pm.response.text()).to.include("checkin");
});
pm.test("Body contains checkout", function () {
    pm.expect(pm.response.text()).to.include("checkout");
});
pm.test("Body contains additionalneeds", function () {
    pm.expect(pm.response.text()).to.include("additionalneeds");
});


pm.test("Response time is less than 600ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(600);
});

```
</details>

This snippet was created to check the status of 200 if the answer received contains the following: Bookingid, firstname, lastname, totalprice, depositpaid, bookingdates, checkin, checkout, addtionalneeds and the server response time is to less 600ms.

<img width="600" alt="Screenshot 2022-08-25 at 12 39 02" src="https://user-images.githubusercontent.com/34375010/186631430-32ff0b1b-b43f-4a48-94cd-580eb16e5b9d.png">

16.Update booking without First name 

:triangular_flag_on_post: Snippets

```
pm.test("Status code is 400", function () {
    pm.response.to.have.status(400);
});
pm.test("Bad Request", function () {
    pm.expect(pm.response.text()).to.include("Bad Request");
});
```
This snippet was created to check the status is 400 and to have "Bad request" in the body.

<img width="600" alt="Screenshot 2022-08-25 at 13 10 42" src="https://user-images.githubusercontent.com/34375010/186638109-b4de81dc-8735-4ab6-929d-5aea473b500e.png">

17.Update booking without no Auth 

:triangular_flag_on_post: Snippets

```
pm.test("Status code is 403", function () {
    pm.response.to.have.status(403);
});
pm.test("Body contain Forbidden", function () {
    pm.expect(pm.response.text()).to.include("Forbidden");
});
```

This snippet was created to check the status is 403 and to have "Forbidden" in the body.

<img width="600" alt="Screenshot 2022-08-25 at 13 13 00" src="https://user-images.githubusercontent.com/34375010/186638583-c3b837cb-4f9c-4c71-8f96-0f2a38d59b2b.png">

18.Partial Update booking after ID

:triangular_flag_on_post: Snippets

```
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Response time is less than 200ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(200);
});
```
This snippet was created to check the status is 200 and server response is less 200ms.

<img width="600" alt="Screenshot 2022-08-25 at 13 16 56" src="https://user-images.githubusercontent.com/34375010/186639394-aca89a9d-3dbb-4434-ae8f-6805852fc0f2.png">

19.Delete booking after ID 

:triangular_flag_on_post: Snippets

```
pm.test("Status code is 201", function () {
    pm.response.to.have.status(201);
});
pm.test("Body contain ", function () {
    pm.expect(pm.response.text()).to.include("Created");
});
```

This snippet was created to check the status is 201 and to have "Created" in the body.

<img width="600" alt="Screenshot 2022-08-25 at 13 19 31" src="https://user-images.githubusercontent.com/34375010/186639897-14d9986e-c8ff-4a01-b723-4c2ab0bc5ae1.png">

20.GET booking after detele

:triangular_flag_on_post: Snippets

```
pm.test("Status code is 200", function () {
    pm.response.to.have.status(404);
});
pm.test("Body matches string", function () {
    pm.expect(pm.response.text()).to.include("Not Found");
});
```
This snippet was created to check the status is 404 and to have "Not found" in the body.

<img width="600" alt="Screenshot 2022-08-25 at 13 21 11" src="https://user-images.githubusercontent.com/34375010/186640236-2aab34c8-2c41-453c-abdc-a773fc1aeed1.png">



