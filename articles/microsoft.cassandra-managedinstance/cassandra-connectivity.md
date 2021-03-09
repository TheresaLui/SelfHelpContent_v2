<properties
	pageTitle="Azure Managed Instance Apache Cassandra connectivity"
	description="Azure Managed Instance Apache Cassandra connectivity"
	service="microsoft.documentdb"
	resource="cassandraClusters"
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
Most users are able to resolve issues with Managed Instance Cassandra connectivity by using the steps below.


## **Recommended Steps**

### **Verify certificates and connectivity with curl**
Make sure you have connectivity with the following `curl` command:

`curl -kv https://<cassandra-api-ip>:9042`   

If this doesn't succeed, you likely have a connectivity issue. If it succeeds, the system is working.

**Note:** Running this command might give the following error: `curl: (60) SSL: certificate subject name '*.managedcassandra.internal.cosmos-test.windows-int.net' does not match target > host name '10.0.8.6'`   
If this occurs, the curl command failed to verify the legitimacy of the server and could not establish a secure connection to it. To learn more about this situation and how to fix it, visit https://curl.haxx.se/docs/sslcerts.html.   

If you get certificate errors, make sure you have all the [Azure certificates](https://docs.microsoft.com/azure/active-directory/fundamentals/certificate-authorities) installed. Refer to your Operating System documentation on how to install them.  

### **I cannot connect with `cqlsh`**
If verifying certificates and connectivity with curl above was successful, try in `cqlsh`:


```
export SSL_VERSION=TLSv1_2
export SSL_VALIDATE=false # disable hostname validation
cqlsh --ssl <host IP> -u <username> -p <password>
```

If you have set up public/private key authentication for the Cassandra API, make sure to supply the private key in the `.cqlshrc` when connecting.

If you still see *Connection error...*:
- Make sure you don't have different certificates set in `~/.cassandra/cqlshrc`. You might need to remove your own certificate, or move the file to a backup location so the certificates installed on your system take precedence.
- Use the Open Source version of `cqlsh`. We have tested our offering only with the open source version and have seen mixed results with the DSE version of `cqlsh`.
- Make sure you have disabled hostname validation in `cqlshrc` with `validate=false`. If you find `valida=true`, you need to change this.

### **I cannot connect with cassandra-stress**
First, verify that certificates and connectivity created with the `curl` command, above, were successful (see previous step, *Verify certificates and connectivity with curl*).  
Most systems are set up so that the certificates installed on the system are also added to the Java system keystore. Make sure this is the case on your system by reviewing your Java installation. Some cassandra-stress installations do not automatically recognize the system-provided keystore.  

In that case, specify the keystore explicitly. For example:

```
cassandra-stress write n=1000000 -rate threads=160 -transport "truststore=/etc/ssl/certs/java/cacerts truststore-password=changeit" -node 10.0.13.5 -mode native cql3 user=cassandra password=cassandra
```
   
If you have set up public/private key authentication for Cassandra, make sure to supply the private key when connecting, as follows:

```
cassandra-stress write n=1000000 -rate threads=160 -transport "truststore=/etc/ssl/certs/java/cacerts truststore-password=changeit" -node 10.0.13.5 -mode native cql3 user=cassandra password=Cassandra keystore=<my-keystore> keystore-password=<my keystore password>
```

### **How do I convert a pem certificate to use as a truststore with Java programs like cassandra-stress?**
The intent is for the installed public certificates to work out-of-the-box with Managed Instance Cassandra offering, and this has been tested as such. So in most cases, the following should not be necessary:  

```
keytool -import -alias mycert -file <certificate file>  -keystore <keystore-file> -storetype PKCS12  -storepass password
```
   
### **I am seeing *com.datastax.driver.core.exceptions.NoHostAvailableException* when running cassandra-stress**

The first error can occur when trying to use cassandra-stress on a multi-dc Cassandra cluster. By default, it creates a non-replicated keyspace, and then fails when trying to access that keyspace from the other datacenter.

You can work around this issue by specifying an additional command-line argument, passing the `schema` parameter:

```
cassandra-stress write n=1000000 -rate threads=160 -transport "truststore=/etc/ssl/certs/java/cacerts truststore-password=changeit" -node $host -mode native cql3 user=cassandra password=cassandra -schema "replication(strategy=NetworkTopologyStrategy, my-dc-westus=3, my-dc-eastus=3)"
```
   
**Note:** The preceding command doesn't update the keyspace if it already exists, so use `CQLSH` to delete `keyspace1` before trying this.


### **My on premise cluster will not connect to Azure Managed Cassandra**

1. 	Verify that you are not connected: 
    - 	Run nodetool <ip of your on prem node> status and observe if the Managed Cassandra data center shows up
    - 	Repeat this for each on-premises node. Some nodes may not connect. If that is the case, follow these steps for each node that can't connect: 
2. 	Review the Cassandra logs of your on premise nodes. Do they show any connection errors regarding managed Cassandra nodes? If so, can you remedy them?
3. 	Make sure to run compatible versions of Cassandra. 
4. 	Make sure Managed Cassandra is running:
    - Run `az managed-cassandra cluster node-status` and observe the status. If the cluster is up, this indicates that it didn’t take your seed nodes. Review the seed nodes. 
    -  If the seed nodes are healthy, there might be connectivity issues.  
    - If the cluster is down, this indicates the seed nodes are not reachable, potentially due to a certificate failure. Double check steps 6 and 7, and then file a ticket.
5. 	Make sure you supplied the proper external seed nodes and external gossip certificates. Check this with `az managed-cassandra cluster show`.
6. 	Make sure you added the Azure Managed Cassandra certificates to the on-premises cluster:
    - Log on to one of the nodes
    - Go to the directory truststore and run: `keytool -list -keystore <your keystore> -storepass <your password> -rfc`
    - Compare carefully the entries with the ones in the `gossipCertificates` field of managed Cassandra. You should be able to find all those certificates.
    - Make sure you have restarted Cassandra so that it takes the new certificates.
7. 	Make sure you have connectivity:
    - Note the `ip pf` one of the Managed Cassanra data nodes 
    - Log on to one of the nodes
    - Run the curl command: `-k https://<ip of one of the managed Cassandra nodes>:7001`
    - The command should return `curl: (35) error:14094412:SSL routines:ssl3_read_bytes:sslv3 alert bad certificate`
8. 	Make sure you provided the correct certificates:
    - Note the `ip pf` of one of the Managed Cassanra data nodes 
    - Log on to one of the nodes
    - Run `openssl s_client -connect<managed Cassandra ip>:7001 -showcerts  -cert <your node3node certificate>` The program should hang after opening an SSL session
    - If you get errors, copy all the certificates from the `gossipCerticate` section of Azure Managed Cassandra into a file and run `openssl s_client -connect<managed Cassandra ip>:7001 -showcerts  -cert <your node3node certificate>  -CAfile <managed-cassandra-certs>`. This shouldn't be necessary, but some operating systems don't have the appropriate certificates installed.
    - If this fails, note the output of the command, double-check the first step again, and create a support ticket that includes the output of that command.

## **Recommended Documents**
[FAQ for Azure Managed Instance Apache Cassandra](https://docs.microsoft.com/azure/managed-instance-apache-cassandra/faq) 
 
