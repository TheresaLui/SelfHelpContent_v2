<properties
	pageTitle="Azure Migrate Collector download and configuration"
	description="Issues and guidance regarding Azure Migrate Collector download and configuration"
	service="microsoft.migrate"
	resource="projects"
	authors="nsoneji"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32593689, 32593688"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
/>

# Azure Migrate Collector download and configuration

## **Recommended steps**

**After upgrading Azure Migrate Collector, all of the details in the Collector configuration page  have disappeared.** 

The Azure Migrate Collector works in a fire and forget model, which means that the discovery is not continuous. When you say ‘Start discovery’ in the appliance, it connects to the vCenter Server, gathers the required metadata (config and performance info of VMs) and sends it to Azure. If there are changes in the on-premises environment, you need to kick off discovery again to ensure it reflects in Azure. The vCenter Server info and migration project info is preserved/cached in the appliance to make it easier for the user to discover the environment again (it is just used to pre-populate the UI), but you can always change it if needed. If you update the appliance, the cached details for vCenter and migration project is cleared, which is why you do not see the details. It has no functional impact as the discovery is already done. Once the update is done, if you want to discover the on-prem environment again, you can key in the details to the updated appliance and kick off a second discovery (either to the existing project or to a new project based on your requirements). Additionally, creation of migration project is a separate step and needs to be manually done in the Azure portal, the appliance does not create the project.

**What version of .NET is required to run dependency agent?**

Microsoft .NET Framework 3.5 or later.

**My Azure Migrate Collector Windows license will be expired soon. Do I need to activate Windows?**

Azure Migrate Collector VM comes with Windows evaluation license and will be valid for six months. Before expiration, we recommend you to download the new Collector from the portal and deploy it. You can use either existing Azure Migrate project or create a new porject for the new Collector. Once your new Collector is deployed, you can decommission the old Collector by simply deleting the old Collector VM. 
Also note that your Collector must be with the latest Windows update. If it is not updated for 60 days, the Collect VM will be shutdown. [Learn more](https://docs.microsoft.com/azure/migrate/concepts-collector#updating-the-collector-vm) about updating the Collector VM.

