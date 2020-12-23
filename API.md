## APIs Details

Base URL for all API endpoints : `http://127.0.0.1:8000/` <br />


i. User - Registration
Create/ Register a new user.

	Endpoint 	: http://127.0.0.1:8000/signup/
	Request Type 	: POST
	Request Params 	: username, email, password, password_2
	Non-mandatory params : invite_code

	Response Http status codes : HTTP_200_OK or HTTP_400_BAD_REQUEST
	
  
ii. User - Login
Obtain authentication token given the user credentials.

	Endpoint 	: http://127.0.0.1:8000/login/
	Request Type 	: POST
	Request Params 	: email (or username) and password
	
	Response 	: { "token": <token> }
	HTTP status code: HTTP_200_OK or HTTP_400_BAD_REQUEST
	
iii. User - Request for Password Reset
Receive an email with password reset link.

	Endpoint 	: http://127.0.0.1:8000/password-reset/
	Request Type 	: POST
	Request Params 	: email
	Request Sample : {"email": "some_email_id@gmail.com"}
	
	HTTP status code: HTTP_200_OK

iv. User - Password Change
  Change the password. Link as recieved from email by above request (iv).
	
	Endpoint 	: http://127.0.0.1:8000/change-password/
	Request Type 	: POST
  
v. User - Retrieve Profile
Retrieve logged in users profile at home page.

	Endpoint 	: http://127.0.0.1:8000/
	Request Type 	: GET
	Request Headers : 
		Authorization : Token <token>
	
	HTTP status code: HTTP_200_OK or HTTP_401_UNAUTHORISED

	
