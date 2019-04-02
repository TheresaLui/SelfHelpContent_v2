<properties
	pageTitle="Azure Migrate Collector configuration and setup"
	description="Issues and guidance regarding Azure Migrate Collector configuration and setup"
	service="microsoft.migrate"
	resource="projects"
	authors="shijojoy"
	ms.author="shijoy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32631897"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId="ecf87d57-c8c4-4009-8d82-f6d50af6c143"
/>

# Azure Migrate Collector configuration and setup

## **Recommended steps**

**After upgrading Azure Migrate Collector, all the details in the Collector configuration page have disappeared.** 

The Azure Migrate Collector works in a fire and forget model, which means that the discovery is not continuous. When you say ‘Start discovery’ in the appliance, it connects to the vCenter Server, gathers the required metadata (configuration and performance information of VMs) and sends it to Azure. If there are changes in the on-premises environment, you need to kick off discovery again to ensure it reflects in Azure. The vCenter Server information and migration project information is preserved/cached in the appliance to make it easier for the user to discover the environment again (it is just used to pre-populate the UI), but you can always change it if needed. If you update the appliance, the cached details for the vCenter Server and migration project are cleared that would results in the details to not appear in the Collector configuration page. It has no functional impact as the discovery is already done. Once the update is done, if you want to discover the on-prem environment again, you can key in the details to the updated appliance and kick off a second discovery (either to the existing project or to a new project based on your requirements). Additionally, creation of migration project is a separate step and needs to be manually done in the Azure portal, the appliance does not create the project.

**What version of .NET is required to run dependency agent?**

Microsoft .NET Framework 3.5 or later.

**My Azure Migrate Collector Windows license will expire soon. Do I need to activate Windows?**

Azure Migrate Collector VM comes with Windows evaluation license which is valid for six months. Before expiration, we recommend you download the new Collector from the portal and deploy it. You can either use existing Azure Migrate project or create a new project for the new Collector. Once your new Collector is deployed, you can decommission the old Collector by simply deleting the old Collector VM. 
Also, note that your Collector must be with the latest Windows update. If it is not updated for 60 days, the Collector VM will be shutdown. [Learn more](https://docs.microsoft.com/azure/migrate/concepts-collector#updating-the-collector-vm) about updating the Collector VM.

**Can I connect the same collector appliance to multiple vCenter servers?**

Yes, a single collector appliance can be used to discover multiple vCenter Servers, but not concurrently. You need to run the discovery one after another.

**How does the collector communicate with the vCenter Server and the Azure Migrate service?**

The collector appliance connects to the vCenter Server (port 443) using the credentials provided by the user in the appliance. It queries the vCenter Server using VMware PowerCLI to collect metadata about the VMs managed by vCenter Server. It collects both configuration data about VMs (cores, memory, disks, NIC etc.) as well as performance history of each VM for the last one month from vCenter Server. The collected metadata is then sent to the Azure Migrate service (over internet via https) for assessment. [Learn more](https://docs.microsoft.com/en-us/azure/migrate/concepts-collector)

**Updating the OS of the Collector VM**

Although the collector appliance has an evaluation license for 180 days, you need to continuously update the OS on the appliance to avoid auto-shut down of the appliance.
If the Collector isn't updated for 60 days, it starts shutting down the machine automatically.
If a discovery is running, the machine won't be turned off, even if 60 days have passed. The machine will be turned off after the discovery completes.
If you've used the Collector for more than 60 days, we recommend keeping the machine updated at all times by running Windows update.


