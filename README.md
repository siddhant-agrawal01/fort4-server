# User Management REST API

A Node.js REST API for user management built with Express.js and MongoDB.

# Deployed Link for Direct Testing
[deployed-link](https://fort4-server.vercel.app/api/users)

## Tech Stack

- Node.js
- Express.js
- MongoDB with Mongoose
- CORS enabled

## Setup

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a .env file with the following variables:
   ```
   PORT=3000
   MONGODB_URL=your_mongodb_connection_string
   ```
4. Start the server:
   ```bash
   npm start
   ```

## API Endpoints

### Get All Users

- **GET** `/api/users`
- Returns: Array of user objects
- Status Codes: 200 (Success), 500 (Server Error)

### Get Single User

- **GET** `/api/users/:id`
- Returns: Single user object
- Status Codes: 200 (Success), 404 (Not Found), 500 (Server Error)

### Create User

- **POST** `/api/users`
- Body:
  ```json
  {
    "name": "siddhant agrawal",
    "email": "siddhant@gmail.com",
    "phone": "1234567890",
    "company": "forty4Corp",
    "address": {
      "city": "mumbai",
      "zipcode": "10001",
      "geo": {
        "lat": 40.7128,
        "lng": -74.0060
      }
    }
}
  ```
- Status Codes: 201 (Created), 400 (Bad Request)

### Update User

- **PUT** `/api/users/:id`
- Body: Same as Create User (all fields optional)
- Status Codes: 200 (Success), 404 (Not Found), 400 (Bad Request)

### Delete User

- **DELETE** `/api/users/:id`
- Status Codes: 200 (Success), 404 (Not Found), 500 (Server Error)



## Testing

You can test the API using tools like Postman.


