 #Post API Testing with Postman
#Table of Contents
#What is an API?
#Types of API Requests
#What is Postman?
#How to Test a POST API using Postman
#Sample Test Case Documentation
#Conclusion

#📍 What is an API?
API (Application Programming Interface) is a set of rules that allows two software programs to communicate with each other.

For example, when you log into a website using Google, an API is used to request your details from Google's servers and send that data back to the website.

💡 Think of an API like a waiter in a restaurant. You tell them your order (the request), they take it to the kitchen (the server), and then bring your food back (the response).

#🔄 Types of API Requests
There are 4 most commonly used types of HTTP methods in API testing:

Method	Purpose
GET	Retrieve data from the server
POST	Send data to the server to create something
PUT	Update existing data on the server
DELETE	Delete data from the server

In this repository, we are focusing on POST API Testing, which is used to create new records.

#🚀 What is Postman?
Postman is a popular API client that allows developers and testers to send API requests, inspect responses, and perform automated testing.

#🔧 Key Features:
User-friendly interface to test APIs

Supports multiple methods: GET, POST, PUT, DELETE

Allows writing test scripts in JavaScript

Supports automated test runs using collections

#🔗 Download Postman

🧪 How to Test a POST API using Postman
✅ Step-by-step Guide
Open Postman

Select Method: Change the method to POST from the dropdown

Enter the API Endpoint (e.g., https://example.com/api/users)

Go to the “Body” Tab:

Choose raw

Set format to JSON

Add your payload like:

json
Copy
Edit
{
  "name": "Mudasir Khan",
  "email": "mudasir@example.com",
  "password": "123456"
}
Click “Send”:

You’ll see the response in the lower section

If successful, you might receive a status 201 Created or 200 OK

#🧾 Headers You Might Need:
Key	Value
Content-Type	application/json
Authorization	Bearer <token> (if secured)

#🧷 Sample Test Case Documentation
Test Case ID	Description	Input Payload	Expected Result	Actual Result	Status
TC01	Register a new user	JSON with name, email, password	Status 201 Created	Status 201 Created	Pass
TC02	Register without email	JSON with missing email	Status 400 Bad Request	Status 400 Bad Request	Pass
TC03	Invalid email format	JSON with incorrect email	Status 422 Unprocessable Entity	-	-

#✅ Conclusion
This project demonstrates how to perform POST API testing using Postman, from setup to writing test cases. Understanding API testing is essential for every QA Engineer, and Postman provides a powerful interface to get started easily.
