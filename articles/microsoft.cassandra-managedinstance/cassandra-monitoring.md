<properties
	pageTitle="Azure Managed Instance Apache Cassandra monitoring"
	description="Azure Managed Instance Apache Cassandra monitoring"
	service="microsoft.documentdb"
	resource="cassandraClusters"
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
Most users can resolve issues with Managed Instance Cassandra monitoring by using the steps below.

## **Recommended Steps**  

### **How do I access Prometheus?**
Copy the value of the field output of the Azure managed-cassandra cluster that shows `-g` <your resource group> and `-c` <your cluster>, the value of the field `prometheusEndpoint`. In a browser, go to https:\\<the ip you just copied>:9443. You might need to approve a certificate error, since we don't currently support hostname validation.  

**Note:** The data on this endpoint is stored only for the last 10 minutes and/or 10 GB of data, whichever limit is reached first. For this reason, we recommend linking this to your own monitoring infrastructure. See your system's documentation on how to link up a Prometheus server. For Prometheus, see [more information](https://prometheus.io/docs/prometheus/latest/federation/).   

### **Not able to access Prometheus**  
- Verify if you have connectivity to the Prometheus endpoint by using  `curl -k https://<prometheus endpoint>:9042` and take note of the error. Make sure that firewalls and connectivity are configured accordingly.

### **Will there be Azure Monitoring Support?**
Azure Monitoring support will be available in a future release.

### **Which metrics are being provided**
We provide all the Cassandra metrics. For example, see [operating metrics](https://cassandra.apache.org/doc/latest/operating/metrics.html). See your installed Prometheus version for an up-to-date list.

### **Prometheus is not running**
Because the probes that Prometheus relies on consisted of stored data, they will eventually catch up.

### **I am missing data**
Review the setup of your monitoring system and increase the interval with which you are scraping data, as needed.  

## **Recommended Documents**
[FAQ for Azure Managed Instance Apache Cassandra](https://docs.microsoft.com/azure/managed-instance-apache-cassandra/faq)
