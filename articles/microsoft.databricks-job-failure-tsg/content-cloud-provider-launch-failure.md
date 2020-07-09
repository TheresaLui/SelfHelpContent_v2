<properties
	pageTitle="Cloud provider launch failure "
	description="Cloud provider launch failure "
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
	articleId="40deb073-550b-4d20-a07b-b482cba3f6dc"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Cloud provider launch failure 

Cloud provider launch failure with error: *The client 'xxx' with object id 'xxx' does not have authorization to perform action 'Microsoft.Network/publicIPAddresses/write' over scope '/subscriptions/xxx...')*

**Troubleshooting and Solution**

Check with customer if they are trying to reuse a Managed RG name from a previously deployed workspace via an ARM template. This is not a supported scenario and will result in cluster start failures because the workspace is not permitted to modify its own MRG.

Possible solution would be to delete the workspace and MRG manually, then redeploy the workspace with the desired name via the ARM template. If the MRG does not delete successfully upon deleting the faulty workspace, you may need to open an IcM. If the customer is blocked and cannot wait for an ICM to manually remove the orphaned MRG, ask the customer if it is possible to deploy with another MRG name.

If issue persists after trying the suggested approach, please discuss issue further with your SME/TA/EEE using [Ava](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/312127/Ava), and [file an IcM](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/333941/Escalate-to-Product-Group-team) if needed.
