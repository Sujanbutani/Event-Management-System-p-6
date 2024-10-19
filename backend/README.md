# Event Management API

This is an Event Management API built using Node.js, Express, and MongoDB. The API allows users to create, view, and RSVP to events. The server is built to serve as a backend for a web or mobile application, handling authentication, event management, and file uploads.

## Features

- **User Authentication**: Users can register, log in, and authenticate using JWT.
- **Event Management**: Users can create, view, and manage events.
- **RSVP Functionality**: Users can RSVP to events, with the system limiting the number of attendees based on the event settings.
- **Image Uploads**: Events can have an image attached to them.

## Technologies Used

- Node.js
- Express
- MongoDB
- Mongoose
- JSON Web Token (JWT)
- Bcrypt.js
- dotenv
- multer
- nodemailer

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Sujanbutani/Event-Management-System-p-6.git

2. Install dependencies:

    ```bash
    npm install

3. .env file

     ```
    MONGO_URI=your_mongo_db_connection_string
    PORT=5000
    IMAGE_UPLOAD_PATH=uploads/
    ```

4. Start the development server:

   ```bash
   npm start
   The server should now be running at http://localhost:5000
   ```

## API Endpoints

### User Authentication
1. Register User (Post) :- localhost:5000/api/auth/register
2. Login User (Post) :- localhost:5000/api/auth/login

### Event Management
1. Event Api (Post) :- localhost:5000/api/events/create
    - Requires JWT token in the Authorization header.
2. Event Api (Get - Allevent) :- localhost:5000/api/events
3. Event Api (Post - rsvp) :-  localhost:5000/api/events/<eventId>/rsvp
4. Event Api (Update) :- localhost:5000/api/events/<event_Id>
5. Event Api (Delete) :- localhost:5000/api/events/<event_Id>

## Environment Variables
- PORT: The port for the server to listen on.
- MONGODB_URI: Your MongoDB connection string.
- JWT_SECRET: Secret key for signing JWT tokens.
- IMAGE_UPLOAD_PATH : image upload folder path