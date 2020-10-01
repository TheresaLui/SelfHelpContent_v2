<properties
  pagetitle="Connecting SQL Managed Instance Azure Arc.&#xD;"
  service="microsoft.azuredata"
  resource="sqlmanagedinstances"
  ms.author="jopilov"
  selfhelptype="Generic"
  supporttopicids="32743975"
  resourcetags=""
  productpesids="17125"
  cloudEnvironments="public, fairfax, usnat, ussec"
  articleid="5a4e6ddb-48c3-4e41-acbe-fad2731ce01b"
  ownershipid="AzureData_Managed_Instance_Azure_Arc" />
# Connecting SQL Managed Instance Azure Arc.

Most users are able to resolve their issues related  to connectivity to a SQL Managed Instance Azure Arc using the recommended documents below.

## **Recommended Steps**

### SQL Connectivity Troubleshooter

The following SQL Server Connectivity Troubleshooter covers most common connection issues and errors and provides steps to resolve them:

- [Solving Connectivity errors to SQL Server](https://support.microsoft.com/help/4009936/solving-connectivity-errors-to-sql-server)

### Test connectivity with Telnet

Make a telnet connection to the Azure Arc Managed Instance to test port and IP address. For example, follow these steps:

1. Find the MI-AA endpoint

   ```bash
   azdata arc sql mi list  #list the endpoint
   ```

   Sample output:

   ```bash
   Name    Replicas    ServerEndpoint      State
   ------  ----------  ------------------  --------
   sqlmi1  1/1         172.29.15.09:31843  Ready
   ```

2. Now use the IP Adress and port:

   ```bash
   telnet 172.29.15.10 31843
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

### Capture Network trace on Linux

1. Determine the name of network adapter using one of the following commands:

   ```bash
   tcpdump -D
   ifconfig
   ```

2. Start the capture and attempt to connect to MI-AA instance.

   **Note:** You may need to change the output folder in the example below:

   ```bash
   sudo tcpdump -w /tmp/tcpdump.pcap -i eth0
   ```

   Sample output:

   ```bash
   tcpdump: listening on eth0, link-type EN10MB (Ethernet), capture size 262144    bytes
   ```

3. After you reproduce the issue, stop the trace by pressing **Ctrl+C**

### Capture Network trace on Windows

1. Start the capture and attempt to connect to MI-AA instance

   ```bash
   netsh trace start persistent=yes capture=yes tracefile=c:\temp\nettrace.etl
   ```

2. Stop the trace after you reproduce the issue

   ```bash
   netsh trace stop
   ```

## Connect to Managed Instance Azure Arc (MI-AA) on an Azure VM

If you are using an Azure virtual machine to host your MI-AA instance, you may  then you need to discover the public IP address in order to connect to the MI-AA endpoint remotely.

1. To locate the external IP address of the VM, use the following command:

   ```bash
   az network public-ip list -g azurearcvm-rg --query "[].{PublicIP:ipAddress}" -o table
   ```

   You can then combine the public IP address with the port to make your connection

1. You may also need to expose the port of the sql instance through the network security gateway (NSG) by adding a rule. To set a firewall rule you will need to know the name of your NSG which you can find out using the command below:

   ```bash
   az network nsg list -g azurearcvm-rg --query "[].{NSGName:name}" -o table
   ```

1. Once you have the NSG name, you can add a firewall rule. The example here create an NSG rule for port 30913 and allows connection from any source IP address. To allow traffic through the (NSG) you will need to add a rule using the following command:

    ```bash
       az network nsg rule create -n db_port --destination-port-ranges 30913     --source-address-prefixes '*' --nsg-name azurearcvmNSG --priority 500 -g     azurearcvm-rg --access Allow --description 'Allow port through for db     access' --destination-address-prefixes '*' --direction Inbound --protocol     Tcp --source-port-ranges '*'
    ```
**Note:** This is not a security best practice! You can lock things down better by specifying a -source-address-prefixes value that is specific to your client IP address or an IP address range that covers your team's or organization's IP addresses. Replace the value of the --destination-port-ranges parameter below with the port number you got from the 'azdata sql instance list' command above.