## [TCP Protocol](https://prayuja-teli.github.io/Blog/TCP)     

#### TCP Protocol - Transmission Control Protocol<br/>
##### Historical origin - May 1974

 ## Discription<br/>

The Transmission Control Protocol provides a communication service at an intermediate level between an application program and the Internet Protocol.TCP is a transport layer protocol in the OSI layer and is used to create a connection between remote computers by transporting and ensuring the delivery of messages over supporting networks and the Internet. Transmission Control Protocol is a connection-oriented communications protocol that facilitates the exchange of messages between computing devices in a network.<br/>

### Features -<br/>

TCP ensures that the data reaches the intended destination in the same order it was sent.<br/>
TCP is connection oriented.<br/> 
TCP requires that connection between two remote points be established before sending actual data.<br/>
TCP provides error-checking and recovery mechanism.<br/>
TCP provides end-to-end communication.<br/>
TCP provides flow control and quality of service.<br/>
TCP operates in Client/Server point-to-point mode.<br/>
TCP provides full-duplex server, i.e. it can perform roles of both receiver and sender.<br/>

## Technical Flag and Handshake Analysis<br/>

#### Urgent Pointer Flag<br/>

The urgent pointer flag is used to identify incoming data as urgent. The incoming segments do not have to wait until the previous segments are consumed by the receiving end but are sent directly and processed immediately. <br/>

#### Acknowledgment Flag<br/>
The acknowledgment flag is used to acknowledge the successful receipt of packets.  If you run a packet sniffer while transferring data using TCP, you will notice every packet you send or receive is followed by an Acknowledgement.<br/>

#### Push Flag<br/>
The push flag (like the urgent flag) exists to ensure that the data is given the priority it deserves and is processed at the sending or receiving end. This flag is used quite frequently at the beginning and end of a data transfer, affecting the way it is handled at both ends<br/>

#### Reset Flag<br/>
The reset flag is used when a segment arrives that is not intended for the current connection. If you were to send a packet to a host in order to establish a connection, and there was no such service waiting to answer at the remote host, the host would automatically reject the request and then send you a reply with the RST flag set.<br/>

#### Synchronization Flag<br/>
The synchronization flag is perhaps the best-known flag in TCP communications. The SYN flag is initially sent when establishing the classic three-way handshake between two hosts.<br/>

#### FIN flag<br/>
The FIN flag is used to tear down the virtual connections created using the previous SYN flag.  The FIN flag always appears when the last packets are exchanged between hosts or connections. It is important to note that when a host sends a FIN flag to close a connection that it may continue to receive data until the remote host has also closed the connection.<br/>




### Share comment and feedback please.
