<properties
	pageTitle="Errors when creating DMS"
	description="Top errors and troubleshooting info for DMS service creation"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="1"
	articleId="service-create-errors"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32743219"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseMigrationService"
/>

# Troubleshooting errors while creating Database Migration Service instance

Most users can resolve issues and error messages that occur when creating a Database Migration Service instance by using the following information.

**Create Service Errors**

**Error:** 

* "SubnetWithExternalResourcesCannotBeUsedByOtherResources" 
* "xxx/NIC-xxxxxxxxxxxx/ipConfigurations/ipconfig cannot be used because it contains external resources."
* "You need to ***delete these external resources*** before deploying into this subnet."

## **Recommended Steps**

* The VNet selected to create a DMS instance in contained external resources such as an application gateway, Azure SQL DB Managed Instance, or hosting environments. DMS can be created in the same VNet, but it needs to be created in a separate subnet. 

**Error message contains some of the following text:**

* The provisioning of deployment for service failed. The Azure Database Migration Service could not be provisioned. One common cause is that the Azure Virtual Network (VNet) does not have internet access due to firewall restrictions. Your VNet Network Security Group (NSG) rules cannot block the following communication ports: 53, 443, 445, 1433, 9354, 12000.
* "VM has reported a failure when processing extension **'CustomScriptExtension'**. Error message: "Finished executing command."
* Download of configuration content from GCS failed.
* Thread running configuration downloader exited, but configuration file was not downloaded.
* Failed to download the configuration for MA; cannot start Agent.
* Error message: "Command execution finished, but failed because it returned a non-zero exit code of: '1'."
The command had an error output of: `actual size (xxxxxx) expected size (xxxxxx)`

## **Recommended Steps** 

* This error occurs most often when the VNet selected to create the DMS instance is blocking connectivity to the metrics and health monitoring end point and/or blocking the following communication ports: 443, 53, 9354, 445, 12000.
* If your DMS subnet is using NSG, make sure that the required outbound NSG rules are added, specifically the outbound rules allowing traffic on port 443 for service tags of Azure Monitor, Service Bus, and Storage. Your NSG should look similar to the following:

	| Priority | Name | Port | Protocol | Source | Destination | Action |
	| ------ | ----- | ---- | ------ | ----- | --------- | --------- |
	| 100 | allowStorage | 443 | Any | VirtualNetwork | Storage | Allow |
	| 200 | AllowServiceBus | 443 | Any | VirtualNetwork | ServiceBus | Allow |
	| 300 | AllowAzureMonitor | 443 | Any | VirtualNetwork | AzureMonitor | Allow |
	| 1000 | block_all_outbound | Any | Any | Any | Any | Deny |
	| 65000 | AllowVnetOutBound | Any | Any | VirtualNetwork | VirtualNetwork | Allow |
	| 65001 | AllowInternetOutBound | Any | Any | Any | Internet | Allow |
	| 65500 | DenyAllOutBound | Any | Any | Any | Any | Deny |


	**Note:** You can also allow regional service tags instead of global service tags, if needed (for example, `Storage.WestUS2`), and TCP protocol instead of Any.


* If the VNet config is allowing port 443, it might be due to firewall blocking the metrics endpoint. To validate this, use the following steps:
  - Create an Azure VM in the same VNet from which the DMS provisioning is being attempted
  - Log in to the VM and try this URL from a browser: https://gcs.prod.monitoring.core.windows.net/
  - The content of the web page should be a response from the API like this:

	`{"Message":"Unable to parse MDS environment/MDS account from path /","Code":"BadRequest","StackTrace":"","Details":null}''`
  
  - If you get an error such as "Page Not Found 404", this means that the firewall config on your network is blocking the endpoints. Contact your network or firewall administrator to identify the IPs/ports that are blocked.
  - If you're able to hit the endpoint and view the content, continue to file the support ticket.
  - **Note:** You can also use these troubleshooting steps for service restart failures. 

## **Recommended Documents**

* [Common Network Configuration Issues](https://docs.microsoft.com/azure/api-management/api-management-using-with-vnet#-common-network-configuration-issues)<br>
* [Overview of prerequisites for using the Azure Database Migration Service](https://docs.microsoft.com/azure/dms/pre-reqs)

**Error:** 

* "ServiceProvisioningDisabledException"
* "The service could not be provisioned. Please contact Microsoft with error code `xxxx-<region_name>`"

## **Recommended Steps** 

* DMS service may not be available in the region you are trying to create an instance. Check [availability by region](https://azure.microsoft.com/global-infrastructure/services/?products=database-migration&regions=all).

**Error:** 

* "ResourceNotPermittedOnDelegatedSubnet"<br>

## **Recommended Steps** 

* The subnet used is a Delegated Subnet. DMS service can't be created in this type of subnet.

## **Recommended Documents**

* [Add, change, or delete a virtual network subnet](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-subnet)
