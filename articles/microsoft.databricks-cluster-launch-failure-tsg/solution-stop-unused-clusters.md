<properties pageTitle="Stop unused clusters"
            description="Stop unused clusters"
            service="Microsoft.Databricks"
            resource="Microsoft.Databricks/workspaces"
            authors="JRMayberry"
            ms.author="rimayber"
            displayOrder=""
            selfHelpType="TSG_Content"
            supportTopicIds=""
            resourceTags=""
            productPesIds=""
            cloudEnvironments="public, fairfax, usnat, ussec"
            articleId="12df9763-c3fb-4b98-9209-a95a7678b0fa"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Stop unused clusters

<!--issueDescription-->
We have accessed your workspace and cluster event logs, and it seems that cluster launch is failing due to Databricks not being able to acquire VMs getting this error:<br>
<br>
*** please paste the error here ***<br>
<br>
To resolve the issue:<br>
1. You can either *stop unused clusters* to release resources.<br>
2. Or if the first suggested solution is not feasible, please *open a case with Azure Subscription Management team* making sure to incluse these details: <br>
    1. Subscription ID<br>
    2. Region<br>
    3. VM type<br>
    4. Current available number of cores<br>
    5. Number of cores to be added.<br>
   <br>
Please check the documents for further details:<br>
<!--/issueDescription-->

## Recommended Documents

1. [Step by step on opening the case](https://docs.microsoft.com/en-us/azure/azure-portal/supportability/per-vm-quota-requests)
2. [Check resource usage against limits](https://docs.microsoft.com/en-us/azure/networking/check-usage-against-limits)