<properties
	pageTitle="Azure Managed Instance Apache Cassandra connectivity"
	description="Azure Managed Instance Apache Cassandra connectivity"
	service="microsoft.cassandra"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32788357,32788358,32788361,32788366,32788368"
	resourceTags=""
	productPesIds="17480"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
	articleId="cassandra-connectivity"
	displayOrder="20"
	category="Connectivity"
	ownershipId="AzureData_AzureManagedInstanceCassandra"
/>

# Azure Managed Instance Apache Cassandra Connectivity Configuration
Most users are able to resolve their Managed Instance Cassandra connectivity issue using the steps below.


## **Recommended Steps**

### **Verify certificates and connectivity with curl**
Make sure you have connectivity
`curl -kv https://<cassandra-api-ip>:9042`   

If this does not succeed, you likely have a connectivity issue. If it succeeds this is normal and shows the system is working.

**!NOTE**: Running this command might give the following error: `curl: (60) SSL: certificate subject name '*.managedcassandra.internal.cosmos-test.windows-int.net' does not match target > host name '10.0.8.6'`   
If this occurs the curl failed to verify the legitimacy of the server and could not establish a secure connection to it. To learn more about this situation and how to fix it, please visit https://curl.haxx.se/docs/sslcerts.html.   

If you get certificate errors make sure you have all the Azure certificates (see https://docs.microsoft.com/azure/active-directory/fundamentals/certificate-authorities) installed. Refer to your Operating System documentation on how to install them.  


### **I cannot connect with cqlsh**
If verifying certificates and connectivity with curl above was successful, try in cqlsh:

```
shell
export SSL_VERSION=TLSv1_2
export SSL_VALIDATE=false # disable hostname validation
cqlsh --ssl <host IP> -u <username> -p <password>
```   

If you have set up public/private key authentication for the Cassandra API make sure to supply the private key in the .cqlshrc when connecting.

If you still see *Connection error...*
- Make sure you do not have different certificates set in `~/.cassandra/cqlshrc` - you might need to remove your own or move the file to some backup location so the certificates installed on your system take precedence
- Use the Open Source version of cqlsh, we have only tested our offering with the Open Source version and heard about mixed results with the DSE version of cqlsh.
- Make sure you have disabled hostname validation in cqlshrc with `validate=false` - if you find `valida=true` it needs to be changed.


### **I cannot connect with Cassandra-stress**
First verify certificates and connectivity with curl above was successful (see previous step *Verify certificates and connectivity with curl*).  
Most systems are setup such that the certificates installed on the system are also added to the Java system keystore. Make sure this is the case on your system by reviewing your Java installation. Some Cassandra-stress installations do not automatically honor the system provided keystore.  

In that case specify it explicitly, for example:

```
shell
cassandra-stress write n=1000000 -rate threads=160 -transport "truststore=/etc/ssl/certs/java/cacerts truststore-password=changeit" -node 10.0.13.5 -mode native cql3 user=cassandra password=cassandra
```   

If you have set up public/private key authentication for Cassandra, make sure to supply the private key when connecting as follows:

```
shell
cassandra-stress write n=1000000 -rate threads=160 -transport "truststore=/etc/ssl/certs/java/cacerts truststore-password=changeit" -node 10.0.13.5 -mode native cql3 user=cassandra password=Cassandra keystore=<my-keystore> keystore-password=<my keystore password>
```


### **How do I convert a pem certificate to use as a truststore with Java programs like cassandra stress?**
The intent is for the installed public certificates to work out of the box with Managed Instance Cassandra offering and this has been tested as such. So in most cases the following should not be necessary.  

```
shell
keytool -import -alias mycert -file <certificate file>  -keystore <keystore-file> -storetype PKCS12  -storepass password
```   

### **I am seeing *com.datastax.driver.core.exceptions.NoHostAvailableException* when running Cassandra-stress**

The first error can occur when trying to use Cassandra-stress on a multi-dc Cassandra cluster. By default it creates a non-replicated keyspace, and then fails when trying to access that keyspace from the other datacenter.

You can work around this issue by specifying additional command line argument, passing the *schema* parameter

```
shell
cassandra-stress write n=1000000 -rate threads=160 -transport "truststore=/etc/ssl/certs/java/cacerts truststore-password=changeit" -node $host -mode native cql3 user=cassandra password=cassandra -schema "replication(strategy=NetworkTopologyStrategy, my-dc-westus=3, my-dc-eastus=3)"
```
**!NOTE**
The above does not update the keyspace if it already exists, so use CQLSH to delete `keyspace1` before trying this


### **My on premise cluster will not connect to Azure Managed Cassandra**

1. 	Verify that you are not connected: 
    - 	Run nodetool <ip of your on prem node> status and observe if the Managed Cassandra data center shows up
    - 	Repeat this for each on-premise node – it can be that some nodes will not connect. If that is the case follow these steps for each node which cannot connect. 
2. 	Review the Cassandra logs of your on premise nodes. Do they show any connection errors in regards to managed Cassandra nodes? If so can you remedy them?
3. 	Make sure to run compatible versions of Cassandra. 
4. 	Make sure Managed Cassandra is running:
    - Run `az managed-cassandra cluster node-status` and observe the status. If the cluster is up it indicates that it didn’t take your seed nodes. Review the seed nodes. 
    -  If the seed nodes are ok there might be connectivity issues.  
    - If the cluster is down this indicates the seed nodes are not reachable, potentially due to a certificate failure. Double check steps 6+7 and then file a ticket.
5. 	Make sure you supplied the proper external seednodes and external gossip certificates. Check with ` az managed-cassandra cluster show `
6. 	Make sure you added the Azure Managed Cassandra certificates to the on-prem cluster:
    - Log onto one of the nodes
    - Go to the directory truststore and run: keytool -list -keystore <your keystore> -storepass <your password> -rfc
    - Compare carefully the entries with the ones in the gossipCertificates field of managed Cassandra. You should be able to find all those certificates.
    - Makes sure you have restarted Cassandra so it takes the new certificates.
7. 	Make sure you have connectivity:
    - Note the ip pf one of the Managed Cassanra data nodes 
    - Log onto one of the nodes
    - Run curl -k https://<ip of one of the managed Cassandra nodes>:7001
    - It should return *curl: (35) error:14094412:SSL routines:ssl3_read_bytes:sslv3 alert bad certificate*
8. 	Make sure you provided the right certificates:
    - Note the ip pf one of the Managed Cassanra data nodes 
    - Log onto one of the nodes
    - Run ` openssl s_client -connect<managed Cassandra ip>:7001 -showcerts  -cert <your node3node certificate> ` - the program should hang after opening an SSL session
    - If you get errors copy all the certificates from the gossipCerticate section of Azure Managed Cassandra into a file and run `openssl s_client -connect<managed Cassandra ip>:7001 -showcerts  -cert <your node3node certificate>  -CAfile <managed-cassandra-certs>` – this should not be necessary but some operating systems do not have the appropriate certificates installed.
    - If this fails note the output of the command, double check the first step again, and create a support ticket with the output of that command.


## **Recommended Documents**
[FAQ for Azure Managed Instance Apache Cassandra](https://docs.microsoft.com/azure/managed-instance-apache-cassandra/faq) 
 
