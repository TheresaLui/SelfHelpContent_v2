<properties
	pageTitle="Slow/unreliable VM launch"
	description="Slow/unreliable VM launch"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="14824574-26f9-41cc-b562-77f6db952b3b"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Slow/unreliable VM launch

Azure VM provisioning on average takes 2.5-3.5 min but sometimes cluster creation take 40+ minutes due to all VM's not provisioned at the sametime. This is due to VM not getting provisioned in timely manner and Databricks having to retry VM requests stragglered over a period of time.

User facing error: *Cluster is running but X nodes could not be acquired.*

**Troubleshooting and Solution**

Check clusters event logs, if you see messages like "Cluster is running but X nodes could not be acquired" followed by cluster resizing, it is a problem with slow VM launch.

To resolve the issue, use a smaller number of nodes but bigger instance types. Retry logic is implemented for cluster manager to retry and get to the desired number of nodes.

If issue persists after trying the suggested approach, please discuss issue further with your SME/TA/EEE using [Ava](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/312127/Ava), and [file an IcM](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/333941/Escalate-to-Product-Group-team) if needed.
