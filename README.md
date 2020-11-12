# To Run the Project

- install dependencies:

  ```bash
   npm install
  ```

- Run the app:
  ```bash
   DEBUG=about-react-dummy-apis:* npm start
  ```

# APIs and Payload

1. **Register**\
   URL: http://localhost:3000/api/user/register\
   Method: POST\
   Payload:
   ```JSON
   {
     "name":"AboutReact",
     "age":40,
     "email":"aboutreact11@gmail.com",
     "address":"P.O. Box 168, 1015 Orci Street",
     "password":"12345"
   }
   ```
   Success Response:
   ```JSON
   {
     "status": "success",
     "data": {
       "name": "AboutReact",
       "age": 40,
       "email": "aboutreact11@gmail.com",
       "address": "P.O. Box 168, 1015 Orci Street",
       "password": "12345"
     },
     "msg": ""
   }
   ```
   Failure Response:
   ```JSON
   {
     "status": "failed",
     "data": {},
     "msg": "User Already Exists"
   }
   ```
2. **Login**\
   URL: http://localhost:3000/api/user/login\
   Method: POST\
   Payload:
   ```JSON
   {
     "email": "aboutreact11@gmail.com",
     "password": "12345"
   }
   ```
   Success Response:
   ```JSON
   {
     "status": "success",
     "data": {
       "name": "AboutReact",
       "age": 40,
       "email": "aboutreact11@gmail.com",
       "address": "P.O. Box 168, 1015 Orci Street",
       "password": "12345"
     },
     "msg": ""
   }
   ```
   Failure Response:
   ```JSON
   {
     "status": "failed",
     "data": {},
     "msg": "No UserId / Password Found"
   }
   ```
3. **Search**\
   URL: http://localhost:3000/api/user/search?q=aboutreact\
   Method: GET\
   User Found Response:
   ```JSON
   {
     "status": "success",
     "data": [
       {
         "name": "AboutReact",
         "age": 40,
         "email": "aboutreact11@gmail.com",
         "address": "P.O. Box 168, 1015 Orci Street",
         "password": "12345"
       }
       ....
       ....
       ....
     ],
     "msg": ""
   }
   ```
   User Not Found Response:
   ```JSON
   {
     "status": "success",
     "data": [],
     "msg": ""
   }
   ```
