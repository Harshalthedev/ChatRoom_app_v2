Real-Time Chat Application - Spring Boot
- A secure, scalable, and feature-rich real-time chat application built using Spring Boot and WebSocket. The application allows users to create and manage chat rooms, communicate instantly, 
and manage their profiles, all while ensuring secure user authentication through Spring Security.This project demonstrates the power of Spring Boot and real-time communication using WebSocket 
in a user-friendly, modern web application.

Features

1. User Authentication & Security
2. Sign Up: Users can create an account by providing their email, name, two security questions, and a password.
3. Login: Users log in securely using their registered email and password.
4. Forgotten Password: If a user forgets their password, they can reset it by answering their security questions and then setting a new password.

Chatroom Management

1. Create Room: Users can create private chat rooms. A unique code is generated upon room creation, which can be shared with others to join the room.
2. Join Room: Users can enter the room code to join any available chat room.
3. Manage Room: Users can manage rooms they have created. This includes options to:
   1. Update the room name.
   2. Delete the room.
   3. Retrieve the room code to share it with others.
4. Profile Management
   1. Update Display Name: Users can change their display name at any time.
   2. Change Password: Users can update their password.
   3. Security Questions: Users can change their answers to security questions for future account recovery.

Real-Time Messaging
   WebSocket Communication: The app enables instant messaging between users in the same chat room through WebSocket communication.

Dashboard Features

Once logged in, users can navigate through the following tabs:
   1. Create Room: Start a new chatroom.
   2. Join Room: Enter a room using its unique code.
   3. Manage Existing Room: View and manage rooms you've created.
   4. Profile Management: Edit your profile details and security settings.
   5. Logout: Log out from the application.

Technologies Used
   1. Backend:
      - Spring Boot: Framework used to build the backend of the application.
      - Spring Security: Provides authentication and authorization functionality.
      - WebSocket: Used for real-time communication between users in a chatroom.
      - REST APIs: For backend interactions like room management and user updates.
  
   2. Frontend:
      - HTML, CSS, JavaScript: For building the user interface and interactive elements.

   3. Database:
       - MySQL (or H2 for development): Stores user data, chat room details, and other necessary information.

   4. Message Security Algorithm
      - To ensure that messages are routed correctly and are only visible to users in the respective room, a custom message security algorithm is implemented.

 How it works:
   1. Message Sending:
      - When a user sends a message in a room, the message and the room code are sent to the server using WebSocket. The data is transmitted in the form of a JSON object.

   2. Message Routing:
     - Upon receiving the message on the server, the backend looks up the room using the room code provided in the JSON object.

   3. Room Validation:
      - The server verifies the room code by searching the database for a room that matches the provided code.

   4. Message Delivery:
      - Once the room is validated, the message is delivered only to users who are currently in that room. The server ensures that the message is visible only to those users, effectively avoiding cross-room messaging and ensuring data security.

  5. No Message Persistence:
     - For security and performance, messages are not stored in the database. Messages are simply relayed to the appropriate users in real-time without being persisted in the database.

 - This ensures that even if there are many rooms and users, messages are confined to their intended room, and no messages leak into other rooms.



  - User Flow:
    - Sign Up:

     - Provide your email, name, password, and answers to two security questions.
      - Login:
           - Use the registered email and password to log in.
       - Dashboard: After logging in, the dashboard will provide the following options:

   - Create Room: 
       - Create a new chat room. A unique code will be generated that you can share with others.
   - Join Room: 
      - Enter a room by providing the unique room code.
   - Manage Room: 
      - View and manage rooms you’ve created (e.g., change the room name, delete the room).
   - Profile Management: 
    - Change your display name, password, and security question answers.
   - Real-Time Chat:
    - Once in a room, communicate with other users instantly through WebSocket-based messaging.
   
   - Logout:
     - You can log out from the dashboard at any time.

   License
     - This project is licensed under the MIT License. See the LICENSE file for more details.

  Contact
     - For any questions or issues, feel free to open an issue or contact me directly at thakareharshal73@gmail.com.

