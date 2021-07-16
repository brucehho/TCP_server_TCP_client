# TCP server and TCP client.


## TCP server:
Create a Qt console application project and choose a new C++ class name as server.<br>
.pro: <br>
QT += network <br>
server.h:<br>

declare startServer() and sendMessageToClients() functions in the public of the class:
void startServer();
void sendMessageToClients(QString message);
Declare the slot functions:
public slots:
	void newClientConnection();
	void socketDisconnected();
	void socketReadReady();
	void socketStateChanged(QAbstractSocket::SocketState state);
Declare two private variables:
private:
	QTcpServer* chatServer;
	QVector<QTcpSocket*>* allClients;

In server.cpp, define the startServer() function.


###


## TCP client:

