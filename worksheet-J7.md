1) What is a packet?
   
   A header, that stores the address of where to send the packet and a payload/data that holds a message or some information to be sent.

2) What is the purpose of an internet layer in the TCP/IP protocol? What do you, as a client, need to specify in this protocol?
   
   Routing those packets to the right places

3) What is the purpose of the transport layer in the TCP/IP protocol? What do you, as a client, need to specify in this protocol?
   
   TCP IP, you want to make sure every packet you send is recieved, it will be slower than dropping some packets. Do you want to be fast or slow? If you are fast, you are less reliable

4) What is the difference between SMTP and HTTP?
   
   HTTP is used for webpages, SMTP stands for email

5) What is the difference between an IP address and a domain name?
   
   The IP Address is 4 bytes, the domain name is the human readable alias of the IP Address

6) How does the operating system use ports?
   
   Ports are integers, where you can specify which port you want to send the information to from the operating system. Allows information traffic to go to specific places, operating system helps choose which port you want.

7) Write code that creates a socket connection to ip address 123.45.678.900 at port 4040. Then, print a color to that socket’s output.
   ```java
   Socket sock = null;
   try
   {
     sock = new Socket("123.45.678.900", 4040);
   }
   catch (Exception e)
   {
     System.err.println("Cannot Connect");
     System.exit(1);
   }
   try
   {
     PrintWriter pw = new PrintWriter(sock.getOutputStream());
     pw.println("red");
     pw.close();
     sock.close();
   }
   catch (Exception e)
   {
     System.err.print("IOException");
     System.exit(1);
   }
   ```
8) What is the difference between a socket’s input stream and its output stream?
   
   Input stream recieves data, Output stream sends data

9) What is the difference between a Socket and a SocketServer?
    
   Only the server can accept connections.

10) How are threads useful with servers? How does a server manage to always be listening for sockets trying to connect?
    
    It allows for parrelelization of the connections in the server. The threads allow for the simulataneous listening for the sockets trying to connect. 
