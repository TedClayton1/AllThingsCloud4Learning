
Net.core.wmem_max is ==a kernel parameter that specifies the maximum size of a write socket buffer in bytes==: 

- **Explanation**
    
    The maximum send window size is defined by net.core.wmem_max. Each socket is given a default send buffer size, but can request up to the maximum size with the setsockopt option SO_SNDBUF. 
    
- **How to change**
    
    You can change the value of net.core.wmem_max in the /etc/sysctl.conf file as root. For example, to set the send window size to 640 KB, you would add the line `net.core.wmem_max=655360`. You can also load the new values into a running kernel without rebooting by entering the command `# sysctl -p` as root. 
    

You can also tune other kernel parameters related to network buffers, such as net.core.rmem_max, which controls the maximum receive buffer size.

Net.core.wmem_max allows an admin with root access to set the send buffer size for all types of connections.