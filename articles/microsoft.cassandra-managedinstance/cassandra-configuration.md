<properties
	pageTitle="Azure Managed Instance Apache Cassandra configuration"
	description="Azure Managed Instance Apache Cassandra configuration"
	service="microsoft.documentdb"
	resource="cassandraClusters"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32788362,32788364,32788352"
	resourceTags=""
	productPesIds="17480"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
	articleId="cassandra-configuration"
	displayOrder="60"
	category="Configuration"
	ownershipId="AzureData_AzureManagedInstanceCassandra"
/>

# Azure Managed Instance for Apache Cassandra configuration
Most users are able to resolve their Managed Instance Cassandra configuration issue using the steps below.



## **Recommended Steps**

### **Cassandra is not running or starting up**
Make sure you are not blocking access to vital Azure services which are needed for Managed Cassandra to work properly:

- Azure Storage
- Azure KeyVault
- Azure Virtual Machine Scale Sets
- Azure Monitoring
- Azure AAD
- Azure Security

### **A data center in a different vnet is not running or starting up**

Make sure the orchestrator node (the one having the Prometheus endpoint) has connectivity to the data center by starting a vm in that vnet and running.   

```
shell
    curl -v https://<ip in the other datacenter>:9443
    curl -v https://<ip in the other datacenter>:8443
```

Only if both return something like:   

```
html
    <html>
    <head><title>400 No required SSL certificate was sent</title></head>
    <body bgcolor="white">
    <center><h1>400 Bad Request</h1></center>
    <center>No required SSL certificate was sent</center>
    <hr><center>nginx/1.14.2</center>
    </body>
    </html>
```
Then everything is set up correctly.  If this is not the case review your vnet-peering configuration and/or firewall settings.

### **Which ports is Managed Cassandra using?**

Cassandra Managed Instances is not using a public IP so the following ports are only accessible from the vnet (or peered vnets./express routes) and *should* not be made accessible on the Internet.

**Cassandra data VM**  
<br> **Port**, *purpose*, Remark
<br> **8443**, *Internal*
<br> **9443**, *Internal*
<br> **7001**, *Gossip*, For Cassandra nodes to talk to each other
<br> **9042**, *Cassandra*, For clients to connect to Cassandra
<br> **7199**, *Internal*

<br>


**Prometheus endpoint**
<br> **Port**, *purpose*, Remark
<br> **9443**, *Prometheus*, Endpoint for Prometheus metrics   


### **DSE 6.0 will not connect to Managed Instances for Cassandra in Hybrid Mode**
We currently only support Apache Cassandra 3.11 – we will have guidance to connect DSE clusters at a later time.


### **Nodetool**
We do not support nodetool directly – instead use (in Azure CLI):

```
azurecli-interactive
az managed-cassandra cluster node-status   -g <my resource group> -c <my cluster> --output table
```

### **sstable tool**
Functionality for that is planned for a later release  


## **Recommended Documents**
[FAQ for Azure Managed Instance Apache Cassandra](https://docs.microsoft.com/azure/managed-instance-apache-cassandra/faq) 
