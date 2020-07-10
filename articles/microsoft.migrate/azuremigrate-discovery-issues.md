<properties
    pageTitle="Discovery issues"
    description="Discovery issues"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="An-mol"
    ms.author="anvar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675749"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="3a672f3a-1f25-4ba7-92f8-cecd50db4097"
	ownershipId="Compute_AzureMigrate"
/>

# Discovery issues

## **Recommended Steps**

### **I don't see the discovered VMs on Azure portal. Server Assessment and Server Migration tiles show a status of "Discovery in progress"**

After starting discovery from the appliance, allow some time for the discovered machines to show up on the Azure portal. It takes around 15 minutes for a VMware discovery, and around 2 minutes per added host for a Hyper-V discovery. If you continue to see "Discovery in progress" even after this time, try the following: 

 - Click **Refresh** on the **Servers** tab. This should show the count of the discovered servers in the Server Assessment and Server Migration tiles.
 - If you are discovering VMware servers, verify that the vCenter account you specified has permissions set correctly and has access granted to at least 1 VM. 
 
 Please note that while you can set the discovery scope to vCenter Server datacenters, clusters, folder of clusters, hosts, folder of hosts, or individual VMs, Azure Migrate is not able to discover VMs if the vCenter account has access granted at vCenter VM folder level. Learn more about scoping discovery [here](https://docs.microsoft.com/azure/migrate/tutorial-assess-vmware#scoping-discovery).


### **Application discovery is not working due to error ID 9013 (temporary profile error).**

Please edit the credentials for the Windows user in username@domain.com format, popularly known as [UPN format](https://docs.microsoft.com/windows/win32/secauthn/user-name-formats). [Learn more](https://docs.microsoft.com/azure/migrate/troubleshoot-appliance-discovery#common-app-discovery-errors) on troubleshooting application discovery issues. 

### **Machines are showing outdated information on the portal. How do I proceed?**

Ensure that the Azure Migrate appliance is up and running. Note that it takes 30 minutes for the latest information to reflect on the Azure Migrate portal. If you still see outdated information, you can perform a refresh using the steps listed [here](https://docs.microsoft.com/azure/migrate/troubleshooting-general#i-do-not-the-latest-information-on-the-on-premise-vms-on-the-portal).


### **What data is collected by Azure Migrate: Server Assessment?**

The Azure Migrate appliance collects metadata about the on-premises VMs, the complete list of metadata collected by the appliance is listed in the following links:

* [Metadata collected using Hyper-V appliance](https://docs.microsoft.com/azure/migrate/migrate-appliance#collected-performance-data-hyper-v)
* [Metadata collected using VMware appliance](https://docs.microsoft.com/azure/migrate/migrate-appliance#collected-metadata-vmware)

Additionally, if you are using the [dependency visualization functionality](https://docs.microsoft.com/azure/migrate/how-to-create-group-machine-dependencies), the dependency agents collect details such as FQDN, OS, IP address, MAC address, processes running inside the VM and the incoming/outgoing TCP connections from the VM.

## Hyper-V VM discovery

### **I do not see the correct disk size on Hyper-V VMs. How do I proceed?**

This can happen if you have disks on SMB storage. In order to detect disk size correctly, it is required that CredSSP delegation is set up from the Azure Migrate appliance to the Hyper-V hosts discovered. [Learn more](https://docs.microsoft.com/azure/migrate/tutorial-prepare-hyper-v#enable-credssp-on-hosts) about how you can do this. 

### **I am facing WinRM errors while validating Hyper-V hosts. What should I do?**

Check whether Hyper-V hosts are ready for discovery by running this [script](https://docs.microsoft.com/azure/migrate/tutorial-prepare-hyper-v#enable-credssp-on-hosts) on the Hyper-V hosts.

### What are the supported host operating systems for Hyper-V VM discovery?

Windows Server 2019, Windows Server 2016 or Windows Server 2012 R2 are the supported Hyper-V host operating systems. You can't assess VMs located on Hyper-V hosts running Windows Server 2012.

### **How can I scope discovery for a multi-tenant environment in Azure Migrate?**

Hyper-V discovery is done using the Hyper-V host and cluster information provided. All VMs running on the hosts added to the Azure Migrate appliance are discovered. Scoping discovery to a single tenant that shares the hosts with other tenants is not supported today in Azure Migrate. 

### **How can I discover a large environment in Azure Migrate?**

Azure Migrate allows you to discover up to 10000 Hyper-V VMs in a single Azure Migrate project. A single appliance supports discovery of up to 5000 VMs. [Learn more](https://docs.microsoft.com/azure/migrate/scale-hyper-v-assessment) about how you can discover a large environment.

## VMware VM discovery

### **How can I scope discovery for a multi-tenant environment in Azure Migrate?**

Azure Migrate allows you to split the discovery of your VMs to ensure that VMs of one tenant are not discovered in another tenant's subscription. [Learn more](https://docs.microsoft.com/azure/migrate/scale-vmware-assessment#plan-discovery-in-a-multi-tenant-environment) about how you can split the discovery in Azure Migrate.

### **How can I discover a large environment in Azure Migrate?**

Azure Migrate allows you to discover up to 35000 VMware VMs in an Azure Migrate project. A single appliance can discover up to 10000 VMs. [Learn more](https://docs.microsoft.com/azure/migrate/scale-vmware-assessment#plan-discovery-in-a-multi-tenant-environment) about how you can discover a large environment.

## Application discovery

### Why does the "Applications discovered" column show a "Discovery in Progress" status? 

Discovery of installed application may take up to 24 hours after you have started discovery in the appliance. Please wait for up to 1 day after starting the discovery for the application details to show up. 

This could also happen if the number of applications found on the machine is 0. This is a known bug and will be fixed in coming releases. 

### Why do I see "Applications discovered" as "Not Supported"? 

The discovery of installed applications is currently only supported for VMware VMs. The message can appear when you have chosen an appliance that you used to discover Hyper-V VMs or physical servers. 


### Is the application discovery using Azure Migrate agentless?  

The application discovery is done without installing any agents or scripts on the machines and VMs. Server Assessment uses the Azure Migrate appliance to perform discovery using the machine credentials provided. The appliance remotely accesses machines using WMI and SSH.

### **What are the privileges required to set up application discovery**

Review the necessary prerequisites for app discovery [here](https://docs.microsoft.com/azure/migrate/migrate-support-matrix-vmware#application-discovery).

