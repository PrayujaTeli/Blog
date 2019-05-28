## [Ip Address](https://prayuja-teli.github.io/Blog/IPAddress)     

#### Ip Address - Internet Protocol Address<br/>

> ## Definition<br/>

An Internet Protocol address (IP address) is a numerical label assigned to each device connected to a computer network that uses the Internet Protocol for communication.<br/>


> ## Description<br/>

IP address is short for Internet Protocol (IP) address. An IP address is an identifier for a computer or device on a TCP/IP network. Networks using the TCP/IP protocol route messages based on the IP address of the destination. 


> ## Function<br/>

An IP address serves two principal functions. It identifies the host, or more specifically its network interface, and it provides the location of the host in the network, and thus the capability of establishing a path to that host. 
 
> ## What is public IP address?<br/>

A public IP address is the address that is assigned to a computing device to allow direct access over the Internet. A web server, email server and any server device directly accessible from the Internet are candidate for a public IP address. A public IP address is globally unique, and can only be assigned to a unique device.

> ## What is private IP address?<br/>

A private IP address is the address space allocated by InterNIC to allow organizations to create their own private network. The computers, tablets and smartphones sitting behind your home, and the personal computers within an organizations are usually assigned private IP addresses. 
 
*Note - InterNIC - Network Information Center*
 
#### How to find IP Address on your system.

1. ip addr show

2. /sbin/ifconfig

3. ifconfig

4. hostname -I 

*Note - It is capital I after hostname.*
 
> ## How Does the Internet Work?

Internet is a global network of computers each computer connected to the Internet must have a unique address. Internet addresses are in the form of nnn.nnn.nnn.nnn where nnn must be a number from 0 - 255. This address is known as an IP address. The program to see if a computer on the Internet is alive is ping.

![Screenshot from 2019-05-28 15-12-43](https://user-images.githubusercontent.com/50698539/58474843-ef6da400-8169-11e9-8009-463e1638e61d.png)

Traceroute and it shows the path your packets are taking to a given Internet destination. Like ping, you must use traceroute from a command prompt.Traceroute will print out a list of all the routers, computers, and any other Internet entities that your packets must travel through to get to their destination.
 
 ![Screenshot from 2019-05-28 17-06-18](https://user-images.githubusercontent.com/50698539/58475270-1e384a00-816b-11e9-8673-51d05f237cf1.png)

1.The message would start at the top of the protocol stack on your computer.<br/>
2.If the message to be sent is long, each stack layer that the message passes through may break the message up into smaller chunks of data.<br/>
3.The packets would go through the Application Layer and continue to the TCP layer. Each packet is assigned a port number. Ports will be explained later, but suffice to say that many programs may be using the TCP/IP stack and sending messages.<br/>
4.After going through the TCP layer, the packets proceed to the IP layer. This is where each packet receives it's destination address, 5.6.7.8.<br/>
5.Now that our message packets have a port number and an IP address, they are ready to be sent over the Internet. The hardware layer takes care of turning our packets containing the alphabetic text of our message into electronic signals and transmitting them over the phone line.<br/>
6.On the other end of the phone line your ISP has a direct connection to the Internet. The ISPs router examines the destination address in each packet and determines where to send it.</br>
7.Eventually, the packets reach computer 5.6.7.8. Here, the packets start at the bottom of the destination computer's TCP/IP stack and work upwards.<br/>
8.As the packets go upwards through the stack, all routing data that the sending computer's stack added (such as IP address and port number) is stripped from the packets.
9. When the data reaches the top of the stack, the packets have been re-assembled into their original form, "Hello computer 5.6.7.8!"<br>

 
 
#### Transmission Control Protocol<br/>

When applications open a connection to another computer on the Internet, the messages they send (using a specific application layer protocol) get passed down the stack to the TCP layer. TCP is responsible for routing application protocols to the correct application on the destination computer.<br/>


#### what happens when user hits any website URL to browser.<br/>

1.Firstly Browser checks cache; if the requested object is in the cache and is fresh, Goes to step 9<br/>
2.The browser asks OS or browser for server's IP address (stored in the cache)<br/>
3.OS makes a DNS lookup and replies the IP address to the browser<br/>
4.The browser opens a TCP connection to the server (this step is much more complex with HTTPS)<br/>
5.The browser sends the HTTP request through TCP connection<br/>
6.The browser receives HTTP response and may close the TCP connection, or reuse it for another request<br/>
7.browser checks if the response is a redirect or a conditional response.<br/>
8.if cacheable, the response is stored in the cache.<br/>
browser decodes the response.<br/>
9.The browser determines what to do with the response.<br/>
10.The browser then uses HTML parser to re-create document structure which is later presented to you on screen. If it finds references to external resources, such as pictures, CSS files, javascript files, these are is delivered the same way as the HTML document itself.<br/>


### Share comment and feedback please.

 
