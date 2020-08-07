<properties 
    pageTitle="How to resolve data drift job take too long to run?"
    description="How to resolve data drift job take too long to run?"
    service="microsoft.machinelearning"
    resource="datadrift"
    authors="WeiLengUSC"
    ms.author="weleng"
    selfHelpType="generic"
    supportTopicIds="32690851"
    resourceTags=""
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
 	articleId="machinelearning-datadrift-driftjobtaketoolongtorun"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# How to resolve data drift job take too long to run?

Data drift job can take too long to run due to multiple reasons, for example, dataset size, compute size, etc. Data drift has enabled auto-termination for data drift job, however, the following steps are recommended to speed up data drift run. 

## **Recommended Steps**

### Vertical scale up compute
Vertical scale up means increasing compute vm size in response to a heavier workload. Provisioning a new aml compute with appropriate VM size and update datadrift monitors compute target setting.

### Vertical scale out compute
If data drift job queuing to long to run that is because there are some jobs are running in current training cluster compute. In order to reduce queuing time, aml compute can scale out by adding more compute node. Open azure machine learning workspace, click  **Compute** -> **Training clusters** -> **[compute target name]** to check the compute status and details. Click **Edit** button to increase Minimum/Maximum number of nodes. 

### Reduce input dataset size
Data drift is monitored through datasets, a baseline dataset and a training dataset. To reduce dataset size, either create dataset from reduced data in data source or use dataset functionality to filter dataset.


## **Recommended Documents**

* [Detect data drift on datasets](https://docs.microsoft.com/azure/machine-learning/how-to-monitor-datasets)<br>
* [Detect data drift on models deployed to Azure Kubernetes Service](https://docs.microsoft.com/azure/machine-learning/how-to-monitor-data-drift)<br>
* [What are compute targets in Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/concept-compute-target)<br>
* [How to create register datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets)<br>
