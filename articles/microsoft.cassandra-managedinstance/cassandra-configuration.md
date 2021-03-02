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
Most users are able to resolve issues with Managed Instance Cassandra configurations by using the steps below.

## **Recommended Steps**

### **Cassandra is not running or starting up**
Make sure you aren't blocking access to vital Azure services that are necessary for Managed Cassandra to work properly:

- Azure Storage
- Azure KeyVault
- Azure Virtual Machine Scale Sets
- Azure Monitoring
- Azure Active Directory
- Azure Security

### **A datacenter in a different VNet is not running or starting up**

Make sure the orchestrator node (the one with the Prometheus endpoint) has connectivity to the datacenter by starting a VM in that VNet and running the following:   

```
shell
    curl -v https://<ip in the other datacenter>:9443
    curl -v https://<ip in the other datacenter>:8443
```

If both commands above return something like the following, this indicates that everything is set up correctly:   

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
If this is not returned in both cases, review your VNet Peering configuration and/or firewall settings.

### **Which ports is Managed Cassandra using?**

Cassandra Managed Instances is not using a public IP, so the following ports are accessible only from VNet (or from peered vnets./express routes) and **should not** be made accessible on the internet.

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


### **DSE 6.0 will not connect to Managed Instances for Cassandra in hybrid mode**
We currently support only Apache Cassandra 3.11. We'll have guidance for connecting DSE clusters at a later time.

### **nodetool**
We do not support `nodetool` directly. Instead, use the following, in Azure CLI:

```
azurecli-interactive
az managed-cassandra cluster node-status   -g <my resource group> -c <my cluster> --output table
```

### **SSTable tool**
Functionality for SSTable tools is planned for a later release. 

## **Recommended Documents**
[FAQ for Azure Managed Instance Apache Cassandra](https://docs.microsoft.com/azure/managed-instance-apache-cassandra/faq) 
