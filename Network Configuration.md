# Network Configuration 

- cat /etc/resolv.conf : gives the dns server address.
- host example.com : shows the addresses of the example.com webpage.
- __Network configuration files__ : 
    - /etc/hosts : This file contains a table of hostnames to IP addresses. It can be used to supplement a DNS server.
    - /etc/resolv.conf : This file contains the IP addresses of the name servers the system should consult in any attempt to resolve names to IP addresses. These servers are often DNS servers.
    - /etc/nsswitch.conf : This file can be used to modify where hostname lookups occur. It contains a particular entry that describes in what order name resolution sources are consulted.
    - __Network Tools__ : 
        - ifconfig :  command stands for interface configuration and is used to display network configuration information.
        - _ip [OPTIONS] OBJECT COMMAND_ : Provides more functionality than ifconfig
            - ip addr show : also performs same as that of ifconfig.
        - route : shows the table of the routes of the network packets sent.
            - above command can be also replaced by ip route show or ip route.
        - ping :  command can be used to determine if another machine is reachable.
            - To limit the number of ping to be sent to the server -c option can be used. example : ping -c 4 google.com(sends 4 ping requests)
        - netstat: command is a powerful tool that provides a large amount of network information. It can be used to display information about network connections as well as display the routing table similar to the route command.
            -  to display statistics regarding network traffic, use the -i option to the netstat command.
            - To use the netstat command to display routing information, use the -r option.
            - ss : command is designed to show socket statistics and supports all the major packet and socket types.
                - Netid	: The socket type and transport protocol
                - State: Connected or Unconnected, depending on protocol
                - Recv-Q: 	Amount of data queued up for being processed having been received
                - Send-Q :	Amount of data queued up for being sent to another host
                - Local Address :	The address and port of the local host’s portion of the connection
                - Peer Address: 	The address and port of the remote host’s portion of the connection
                - -s option, displays mostly the types of sockets, statistics about their existence and numbers of actual packets sent and received via each socket type.
        - dig command :  performs queries on the DNS server to determine if the information needed is available on the server.
        - host : command works with DNS to associate a hostname with an IP address. 
            - host -a example.com : shows the comperehensive list of all DNS servers.
        - ssh :  command allows you to connect to another machine across the network, log in and then perform tasks on the remote machine.
            - ssh bob@test(username@hostname) - to request ssh connection.
            - RSA Key Fingerprint errors can be removed by removing ~/.ssh/known_hosts file from your local system (or just remove the entry for that one machine) and try to connect again.