
## Task From Fatura


- First clone This Project In your local 
- second run `composer install` && `composer update`
- run `php artisan migrate` 
- run `php artisan serve`
- after these open postman to test !!
- Create a user account for testing on postaman 
## First 
- Create a user account for testing
- Endpoint : 127.0.0.1:8000/api/register
- Method: POST
- Payload:
- name: Ahmed
- email: Ahmed@email.com
- password: Ahmed
- password_confirmation: Ahmed
## Second
- User login
- Endpoint : 127.0.0.1:8000/api/login
- Method: POST
- Payload:
- email: Ahmed@email.com
- password: Ahmed
## third
- Accessing an unprotected route
- Endpoint : 127.0.0.1:8000/api/open
- Method: GET
- This Message Will Show  "This data is open and can be accessed without the client being authenticated"
## Fourth
- Access a protected endpoint
- Endpoint : 127.0.0.1:8000/api/open
- Method: GET
- Payload:
- Authorization: Bearer insert_user_token_here
- This Message Will Show "Only authorized users can see this"
## Fifth
- Get the authenticated user data
- Endpoint : 127.0.0.1:8000/api/user
- Method: GET
- Payload:
- Authorization: Bearer insert_user_token_here
- Will retreve data
## sixth
- Use invalid token to access a users data
- Endpoint : 127.0.0.1:8000/api/user
- Method: GET
- Payload:
- Authorization: Bearer thistokeniswrong
- This Message Will Show "Token is Invalid"
## seventh
- Accessing a protected route without a token
- Endpoint : 127.0.0.1:8000/api/closed
- Method: GET
- This Message Will Show "Authorization Token not found"

