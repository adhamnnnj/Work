# TCP chatroom
This code implements a simple multi-client chatroom using Python sockets and threading.

Client Code (clientchatroom.txt)
Runs two threads:
Receiving thread: Listens for incoming messages and prints them. If the server requests a name ("name?"), it sends the user’s name.
Sending thread: Continuously takes user input and sends messages prefixed with the user’s name.

Server Code (serverChatroom.txt)
For each client:
Asks for their alias (name), stores it, and notifies others.
Starts a new thread to handle incoming messages from that client.
Broadcast function: Sends messages to all connected clients.
Removes clients that disconnect or cause errors, and notifies the chatroom.

How it works overall
Each client connects to the server and joins the chat using an alias.
Messages from any client are sent to all others via the server.
Threading allows multiple clients to communicate concurrently.
Let me know if you want a diagram or a more technical breakdown.
