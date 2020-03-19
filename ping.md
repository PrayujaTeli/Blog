## [ping command](https://prayuja-teli.github.io/Blog/ping)     

 ## History 

Developed by - Michael Muss<br/>
Development date - 1983<br/>
Type - network data packet command<br/>


 ## Definition

Ping is a computer network administration  system software designed to help to analyze, configure, optimize or maintain a computer  used to test the reachability of a host on an Internet Protocol (IP) network.

 ## Description - 

Ping uses ICMP(Internet Control Message Protocol) to send an ICMP echo message to the specified host if that host is available then it sends ICMP reply message.

## Execution 

Open terminal - Ctrl + Alt + T <br/>
Syntax - ping argument <br/>
Argument - Input given to a command line to process that input with the help of given command.<br/>

#### Note - If ping command won't work try typing sudo infornt of ping command.<br/>

 ## Some Basic Ping functions<br/>

Here are some basic ping functions that you will be using to check the performance of your network:<br/>

### Pinging the host for availability<br/>

You can check if a host is alive or not through the following ping command:<br/>
Syntax - $ ping host-name/IP<br/>
Press Ctrl+C for breaking the command<br/>


Pinging Global host for availability<br/>
Eg - Host - www.google.com<br/>
Syntax - $ ping www.google.com<br/>
Press Ctrl+C for breaking the command<br/>

output will look something like this -<br/>
<br/>
PING google.com (172.217.22.206) 56(84) bytes of data.<br/>
64 bytes from muc11s01-in-f14.1e100.net (172.217.22.206): icmp_seq=1 ttl=53 time=40.2 ms<br/>
64 bytes from muc11s01-in-f14.1e100.net (172.217.22.206): icmp_seq=2 ttl=53 time=41.8 ms<br/>
64 bytes from muc11s01-in-f14.1e100.net (172.217.22.206): icmp_seq=3 ttl=53 time=47.4 ms<br/>
64 bytes from muc11s01-in-f14.1e100.net (172.217.22.206): icmp_seq=4 ttl=53 time=41.4 ms<br/>
^C<br/>
--- google.com ping statistics ---<br/>


### Set ping timeout<br/>
You can set a time limit after which ping will exit; no matter how many ping packets are sent or received:<br/>

$ ping -w timeinseconds hostname/ip<br/>

Here user doesn't have to press Ctrl + c to stop execution of running command.
 
### Controlling the size of packets send:<br/>
Ealier a default sized packets were sent to a host but we can send light and heavy packet by using -s option.<br/>

 ping -s 40 -c 5 www.google.com <br/>
 
 ## Basic ping options :<br/>
#### -d<br/>
Set the SO_DEBUG socket option.<br/>
#### -l<br/>
Loose source route. Use this option in the IP header to send the packet to the given host and back again. Usually specified with the -R option.<br/>
#### -L<br/>
Turn off loopback of multicast packets. Normally, if there are members in the host group on the out- going interface, a copy of the multicast packets will be delivered to the local machine.<br/>
#### -n<br/>
Show network addresses as numbers. ping normally displays addresses as host names.<br/>
#### -r<br/>
Bypass the normal routing tables and send directly to a host on an attached network. If the host is not on a directly-attached network, an error is returned. This option can be used to ping a local host through an interface that has been dropped by the router daemon.<br/>
#### -R<br/>
Record route. Sets the IP record route option, which will store the route of the packet inside the IP header. The contents of the record route will only be printed if the -v option is given, and only be set on return packets if the target host preserves the record route option across echos, or the -l option is given.<br/>
#### -v<br/>
Verbose output. List any ICMP packets, other than ECHO_RESPONSE, that are received.<br/>
#### -i interface_address<br/>
Specify the outgoing interface address to use for multicast packets. The default interface address for multicast packets is determined from the (unicast) routing tables.<br/>
#### -I interval	<br/>
Specify the interval between successive transmissions. The default is one second.<br/>
#### -t ttl<br/>
Specify the IP time to live for unicast and multicast packets. The default time to live for unicast packets is set with ndd (using the icmp_def_ttl variable). The default time to live for multicast is one hop.<br/>
#### host<br/>
The network host.<br/>
#### packetsize<br/>
Specified size of packetsize. Default is 64.<br/>
#### count<br/>
Amount of times to send the ping request.<br/>
 
 
 Share comment and feedback please.


 
