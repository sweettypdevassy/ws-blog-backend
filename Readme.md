# WebSocket Chat Application

WebSocket Chat Application is a simple chat server built using the Jakarta WebSocket API. This application allows multiple clients to connect and communicate in real-time through WebSocket connections, enabling an interactive chat experience.

## Technologies Used

- Java: The programming language used for the application.

- Jakarta WebSocket API: Provides the WebSocket functionality.

- Open Liberty: The server runtime environment for deploying the application.

## Prerequisites

 Before you begin, ensure you have the following installed:

- Java Development Kit (JDK) version 11 or higher.

## Installation

To set up the application, follow these steps:

1. Clone the repository:

    ```
    git clone https://github.com/sweettypdevassy/ws-blog-backend.git
    cd ws-blog-backend
    ```

2. Run the project using Maven:
    ```
    mvn liberty:dev
    ```

## Running the Application

Once the application is running, you can test the chat functionality:

### Test the Chat Application

1. Open two browser windows.

2. Use the browser console as the WebSocket client. In Chrome, press F12 and navigate to the Console tab.

3. Connect each tab to the WebSocket server by running the following JavaScript code:

    ```
    const ws = new WebSocket("ws://localhost:9080/ws-blog/chat");
    ws.onopen = () => console.log("Connected to chat"); 
    ws.onmessage = (msg) => console.log("Message from server: " + msg.data); 
    ws.onclose = () => console.log("Disconnected from chat");
    ```

4. Send a message to the chat using the following function:

    ```
    function sendMessage(text) { ws.send(text); } // Example: To send a message, type sendMessage("Hello from user!");
    ```

### Start Chatting

- In each console, use sendMessage("Your message") to send messages.

- You should see messages from both users appearing in both browser consoles, creating a live chat experience.

## Contributing

Contributions are welcome! If you have suggestions for improvements or new features, please fork the repository and submit a pull request.