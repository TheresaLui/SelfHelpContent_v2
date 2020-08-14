<properties
    pageTitle="Discovery issues"
    description="Discovery issues"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="An-mol"
    ms.author="hamusa"
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

After starting discovery from the appliance, allow some time for the discovered machines to show up on the Azure portal. It takes around 15 minutes for a VMware discovery, and around 2 minutes per added Hyper-V host or physical server. If you continue to see "Discovery in progress" even after this time, try the following: 

 - Ensure the "Save and start discovery" operation has completed.
 - Click **Refresh** on the **Servers** tab. This should show the count of the discovered servers in the Server Assessment and Server Migration tiles.
 - If you are discovering VMware servers, verify that the vCenter account you specified has permissions set correctly and has access granted to at least 1 VM. 
 
 Please note that while you can set the discovery scope to vCenter Server datacenters, clusters, folder of clusters, hosts, folder of hosts, or individual VMs, Azure Migrate is not able to discover VMs if the vCenter account has access granted at vCenter VM folder level. Learn more about scoping discovery [here](https://docs.microsoft.com/azure/migrate/tutorial-assess-vmware#scoping-discovery).


### **What are the prerequisites to set up application discovery**

Review the necessary prerequisites for app discovery [here](https://docs.microsoft.com/azure/migrate/migrate-support-matrix-vmware#application-discovery-requirements).


### **I deployed more than one appliances to discover my machines. When I try to migrate the machines, I only see those corresponding to one of the appliance.**
If there are multiple appliances set up, it is required there is no overlap among the VMs on the vCenter accounts provided. A discovery with such an overlap is an unsupported scenario. [Learn more](https://go.microsoft.com/fwlink/?linkid=2138867) about how to plan discovery for multiple appliances.


### **Machines are showing outdated information on the portal. How do I proceed?**

Ensure that the Azure Migrate appliance is up and running. Note that it takes up to 30 minutes for Hyper-V and VMware VMs, and 3 hours for physical servers for the latest information to reflect on the Azure Migrate portal. If you still see outdated information, you can perform a refresh using the steps listed [here](https://docs.microsoft.com/azure/migrate/troubleshooting-general#i-do-not-the-latest-information-on-the-on-premise-vms-on-the-portal).


### **What data is collected by Azure Migrate: Server Assessment?**

The Azure Migrate appliance collects metadata about the on-premises VMs, the complete list of metadata collected by the appliance is listed in the following links:

* [Metadata collected using Hyper-V appliance](https://docs.microsoft.com/azure/migrate/migrate-appliance#appliance---hyper-v)
* [Metadata collected using VMware appliance](https://docs.microsoft.com/azure/migrate/migrate-appliance#appliance---vmware)
* [Metadata collected using physical appliance](https://docs.microsoft.com/azure/migrate/migrate-appliance#appliance---physical)

Additionally, if you are using the [dependency visualization (agent-based) functionality](https://docs.microsoft.com/azure/migrate/how-to-create-group-machine-dependencies), the dependency agents collects FQDN, OS, IP address, MAC address, processes running inside the VM and the incoming/outgoing TCP connections from the VM.


### **I do not see the right disk size on Hyper-V VMs. How do I proceed?**

This can happen if you have disks on SMB storage. In order to detect the disks correctly, it is required that CredSSP delegation is set up from the Azure Migrate appliance to the Hyper-V hosts discovered. [Learn more](https://docs.microsoft.com/azure/migrate/tutorial-prepare-hyper-v#enable-credssp-to-delegate-credentials) about how you can do this. 


### **How can I scope discovery for a multi-tenant Hyper-V environment in Azure Migrate?**

Hyper-V discovery is done using the Hyper-V host and cluster information provided. All VMs running on the hosts added to the Azure Migrate appliance are discovered. Scoping discovery to a single tenant that shares the hosts with other tenants is not supported today in Azure Migrate. 

### **How can I discover a large environment in Azure Migrate?**

Refer to the linked documentation to learn more about planning discovery of large [VMware](https://docs.microsoft.com/azure/migrate/scale-vmware-assessment), [Hyper-V](https://docs.microsoft.com/azure/migrate/scale-hyper-v-assessment) and [physical](https://docs.microsoft.com/azure/migrate/scale-physical-assessment) environments.

### **I am facing WinRM errors while validating Hyper-V hosts. What should I do?**

Check whether Hyper-V hosts are ready for discovery by running this [script](https://docs.microsoft.com/azure/migrate/tutorial-prepare-hyper-v#run-the-script) on the Hyper-V hosts.

### What are the supported host operating systems for Hyper-V VM discovery?

Find details [here](https://docs.microsoft.com/azure/migrate/migrate-support-matrix-hyper-v#hyper-v-host-requirements).


### **Application discovery is not working due to error ID 9013 (temporary profile error).**

Please edit the credentials for the Windows user in username@domain.com format, popularly known as [UPN format](https://docs.microsoft.com/windows/win32/secauthn/user-name-formats). [Learn more](https://docs.microsoft.com/azure/migrate/troubleshoot-appliance-discovery#common-app-discovery-errors) on troubleshooting application discovery issues. 

