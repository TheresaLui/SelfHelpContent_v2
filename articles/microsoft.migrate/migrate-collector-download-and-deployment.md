<properties
	pageTitle="Azure Migrate Collector download and deployment"
	description="Issues and guidance regarding Azure Migrate Collector download and deployment"
	service="microsoft.migrate"
	resource="projects"
	authors="shijojoy"
	ms.author="shijoy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32631898,32631941,32631942"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId="ecf87d57-c8c4-4009-8d82-f6d54af6c540"
/>

# Azure Migrate Collector download and deployment

## **Recommended Steps**

* **What version of .NET is required to run dependency agent?**

	Microsoft .NET Framework 3.5 or later.

* **My Azure Migrate Collector Windows license will expire soon. Do I need to activate Windows?**

	Azure Migrate Collector VM comes with Windows evaluation license which is valid for six months. Before expiration, we recommend you download the new Collector from the portal and deploy it. You can either use existing Azure Migrate project or create a new project for the new Collector. Once your new Collector is deployed, you can decommission the old Collector by simply deleting the old Collector VM. 

	Also, note that your Collector must be with the latest Windows update. If it is not updated for 60 days, the Collector VM will be shutdown. [Learn more](https://docs.microsoft.com/azure/migrate/concepts-collector#updating-the-collector-vm) about updating the Collector VM.

* **I am getting this error when deploying Azure Migrate Collector OVF file: The provided manifest file is invalid: Invalid OVF manifest entry.**

1. Verify if Azure Migrate Collector OVF file is downloaded correctly by checking its hash value. Refer to the [article](https://docs.microsoft.com/azure/migrate/tutorial-assessment-vmware#verify-the-collector-appliance) to verify the hash value. If the hash value is not matching, download the OVF file again and retry the deployment.
2. If it still fails and if you are using VMware vSphere Client to deploy the OVF, try deploying it through vSphere Web Client. if it still fails, try using different web browser.
3. If you are using vCenter Server 6.5, then try to deploy the Collector on ESXi host directly:

	* Go to ESXi host web client using https://<hostip>/ui and login
	* Go to Virtual machines -> Create/Register VM -> Deploy a virtual machine from an OVF or OVA ->Deploy ova
	* Power on the VM after deployment

4. If the issue still persists, please contact Azure Migrate support team.
