# TCP server and TCP client.
A application like an internet live chat room.  
We need two programs **client** and **server**: a client program for users to use to  send and receive messages from other users. A server program that connects all  clients and delivers their messages.  
In **client** application needed a visually enjoyable and easy to use GUI for user to read and compose their messages. Therefore the client application as a Qt widgets application. It simply connects the server, sends the messages entered by the user, and prints out everything that the server sends to it.  
The **server** application just handles everything silently behind the scenes, it doesn’t need any user interface, so we only need it as a Qt console application.  
  
## TCP server:
TCP networking is typically used for programs that require every piece of data to be sent and received in sequence. It also ensures that the client receives the data and sends a notification to the server.  
``` 
QT += network
```  
```
// qtcp module.
#include <QTcpServer>
#include <QTcpSocket>
#include <QVector>
#include <QDebug>
```
```
//declare startServer() and sendMessageToClients() functions
//in the public of the class:
	void startServer();
    void sendMessageToClients(QString message);
```
```
// declare the slot functions
//declare 2 private variable
```  
In main.cpp  
```
	server* myServer = new server();
	myServer->startServer();
```
<img src="https://raw.githubusercontent.com/brucehho/TCP_server_TCP_client/main/example/Screenshot%202021-07-15%20124802.jpg" width="500" height="80"/>


## TCP client:
Before we can run the client program, we must first run the server program that we created. Then build and run the client program. After opening the program, click on the "Connect" button. After successfully connecting to the server, type a word in the edit widget located at the bottom and press the send button. This time the display window will appear with the word you wrote.  
<img src="https://raw.githubusercontent.com/brucehho/TCP_server_TCP_client/main/example/Screenshot%202021-07-15%20212829.jpg" width="350" height="300"/>  
  
Go to the server program to check if anything printed on the **terminal window**.  
<img src="https://raw.githubusercontent.com/brucehho/TCP_server_TCP_client/main/example/Screenshot%202021-07-15%20161223.jpg" width="600" height="150"/>  

 
