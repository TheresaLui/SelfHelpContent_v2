<properties
 pageTitle="Miscellaneous Error Codes"
 description="Miscellaneous Error Codes"
 service="Microsoft.RecoveryServices"
 resource="Microsoft.RecoveryServices/Vaults"
 authors="StorageMediaEdge_Backup"
 ms.author="StorageMediaEdge_Backup"
 displayOrder=""
 selfHelpType="TSG_Content"
 supportTopicIds=""
 resourceTags=""
 productPesIds=""
 cloudEnvironments="public, fairfax, usnat, ussec"
 articleId="aacadb5a-5cfb-42eb-834b-b3552acfefbd"
 ownershipId="StorageMediaEdge_Backup"
/>

# Miscellaneous Error Codes


## Review Known issues

Make sure you review   
 [Miscellaneous](https://supportability.visualstudio.com/AzureBackup/_wiki/wikis/AzureBackup?pagePath=%2FTroubleshoot%2FAzure%20VM%2FAzure%20VM%20Error%20Codes%2FAzureBackup%252DIaaSVM%252DMiscellaneous%252Dfailures)    
[User errror codes](https://supportability.visualstudio.com/AzureBackup/_wiki/wikis/AzureBackup/184547/Azure-VM-Error-Codes)



## Collect  and Analyze  Guest Agent and Extension Logs 

Collect **Guest Agent** and **Extensions** Logs then ask AVA/TA/PG if needed:  

 - Check if the customer has **granted permission** for collecting logs.  
Go to (**ASC -> Case Overview -> Permissions -> Log Permission (Granted)**).

 - Method 1 (**collecting logs using ASC**):  
Go to (**ASC -> Resource Explorer for VM -> Diagnostics tab -> Inspect IaaS Disk -> click + Create Report**).  
In the **Create Report** window, select **Diagnostic** from the Mode drop-down option and enter the 	required details then click **Run**.

 - Method 2 (**collecting logs manually from customers VM**)  
If the Inspect IaaS Disk isn't working or you need a more 	comprehensive set of logs then collect the logs (***after getting the customer permission***) from the 	following locations:

  - For **Windows Azure VM**  
 C:\Packages\Plugins\(get plugins based on current issue)  
 C:\WindowsAzure\Logs\Plugins\  
 C:\WindowsAzure\Logs\WaAppAgent.log  

  - For **Linux Azure VM**  
 /var/lib/waagent/*.xml  
 /var/log/waagent.log*  
 /var/log/azure/*  


## Analyze the Backup  from service side to try to isolate the issue  

Using the query  on kusto shared on previous steps :  

union cluster('mabprod1').database('MABKustoProd1').TraceLogMessage,   
cluster('mabprodweu').database('MABKustoProd').TraceLogMessage,  
cluster('mabprodwus').database('MABKustoProd').TraceLogMessage   
    | where TaskId == "***TASKID***"  
    | project PreciseTimeStamp,  Message, Level  
    | order by PreciseTimeStamp desc  

Use the Level color code to help you track what errors might be happening in the Backup Job. After taking a look into the logs  .  

Level 1 lines(black)  contains exception,  and  should be review to see if they are the cause of backup process to stop . Some exception can be expected and  handle and backup continue , make sure they are the cause of the errorcode that is raised for failure.  


