<properties
  pagetitle="Connecting SQL Managed Instance Azure Arc."
  service="microsoft.azuredata"
  resource="sqlmanagedinstances"
  ms.author="jopilov"
  selfhelptype="Generic"
  supporttopicids="32743975"
  productpesids="17125"
  cloudenvironments="public, fairfax, mooncake, blackforest, ussec, usnat"
  articleid="5a4e6ddb-48c3-4e41-acbe-fad2731ce01b"
  ownershipid="AzureData_Managed_Instance_Azure_Arc" />
# Connecting SQL Managed Instance Azure Arc.

Most users are able to resolve their issues related  to connectivity to a SQL Managed Instance Azure Arc using the recommended documents below.

## **Recommended Steps**


### SQL Connectivity Troubleshooter

The following SQL Server Connectivity Troubleshooter covers most common connection issues and errors and provides steps to resolve them:
[Solving Connectivity errors to SQL Server](https://support.microsoft.com/en-us/help/4009936/solving-connectivity-errors-to-sql-server)

### Test connectivity with Telnet
Make a telnet connection to the Azure Arc Managed Instance to test port and IP address
#### Example: 

1. Find the MI-AA endpoint

   ```bash
   $ azdata arc sql mi list  #list the endpoint

   Name    Replicas    ServerEndpoint      State
   ------  ----------  ------------------  --------
   sqlmi1  1/1         172.29.15.09:31843  Ready
   ```

2. Now use the IP Adress and port:

   ```bash
   $ telnet 172.29.15.10 31843
   ```

   Sample output:

   ```bash
   Trying 172.29.15.09...
   Connected to 172.29.15.09.
   Escape character is '^]'.   # Ctrl + ]
   telnet> quit
   Connection closed.
   ```

### Capture a network trace
You can capture a network trace on both server and client system for further analysis.
 
#### Example to Capture Network trace on Linux: 

1. Determine the name of network adapter using one of the following commands:

   ```bash
   tcpdump -D
   ifconfig
   ```
   
2. Start the capture and attempt to connect to MI-AA instance

   ```bash
   $ sudo tcpdump -w /tmp/tcpdump.pcap -i eth0
   tcpdump: listening on eth0, link-type EN10MB (Ethernet), capture size 262144    bytes
   ```

3. After you reproduce the issue, stop the trace by pressing **Ctrl+C**

#### Example to Capture Network trace on Windows: 

1. Start the capture and attempt to connect to MI-AA instance

   ```bash
   netsh trace start persistent=yes capture=yes tracefile=c:\temp\nettrace.etl
   ```

2. Stop the trace after you reproduce the issue
   
   ```bash
   netsh trace stop
   ```