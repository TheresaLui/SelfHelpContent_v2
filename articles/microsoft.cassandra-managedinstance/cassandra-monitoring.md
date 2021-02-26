<properties
	pageTitle="Azure Managed Instance Apache Cassandra monitoring"
	description="Azure Managed Instance Apache Cassandra monitoring"
	service="microsoft.cassandra"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32788356,32788365"
	resourceTags=""
	productPesIds="17480"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
	articleId="cassandra-monitoring"
	displayOrder="80"
	category="Configuration"
	ownershipId="AzureData_AzureManagedInstanceCassandra"
/>


# Azure Managed Instance for Apache Cassandra monitoring
Most users are able to resolve their Managed Instance Cassandra monitoring issue using the steps below.

## **Recommended Steps**  

### **How do I access Prometheus**
Copy the value of the field output of az managed-cassandra cluster show -g <your resource group> -c <your cluster> the value of the field prometheusEndpoint. In a browser go to https:\\<the ip you just copied>:9443. You might need to approve of a certificate error since we do not support hostname validation at this point.  

**Note:** The data on this endpoint is only stored for the last 10 minutes and/or 10 GB of data - whichever is reached first. For this reason we recommend to link this to your own monitoring infrastructure. Refer to the documentation of your system on how to link up a prometheus server. For Prometheus itself you can find this information at https://prometheus.io/docs/prometheus/latest/federation/.   


### **Not able to access Prometheus**  
- Verify if you have connectivity to the prometheus endpoint using  `curl -k https://<prometheus endpoint>:9042` and take note of the error. Make certain firewalls and connectivity is configured accordingly.

### **Will there be Azure Monitoring Support**
Azure Monitoring support will be coming in one of the future releases.

### **Which metrics are being provided**
We provide all the cassandra metrics you might find on a page like https://cassandra.apache.org/doc/latest/operating/metrics.html Refer to the installed Prometheus for an up-to date list.

### **Prometheus is not running**
Since the probes Prometheus relies upon is store data, it will eventually catch up.

### **I am missing data**
Please review the setup of your monitoring system and increase the interval you are scraping data as needed.  


## **Recommended Documents**
[FAQ for Azure Managed Instance Apache Cassandra](https://docs.microsoft.com/azure/managed-instance-apache-cassandra/faq)