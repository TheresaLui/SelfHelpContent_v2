<properties
  pageTitle="networkwatcher/connectionmonitor"
  description="networkwatcher/connectionmonitor"
	service="microsoft.network"
	resource="networkwatcher"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32606420"
	resourceTags=""
	productPesIds="16160"
	cloudEnvironments="public,fairfax,mooncake"
	articleId="67d46e6c-ee76-4433-8e11-1adcbdef0e12"
/>

# Connection Monitor

## **Recommended Steps**

### **Internal Server Error while trying to create Connection Monitor**

* Check if Network Watcher is installed in the region you are trying to create Connection Monitor in. [Use this link to install Network Watcher in a region](https://docs.microsoft.com/azure/network-watcher/network-watcher-create).
* Check if Network Watcher is supported in the region you are trying to create Connection Monitor in <br>
* Ensure that your source VM has Network Watcher extension installed without issues and is in the same subscription in which you are trying to create the Connection Monitor <br>
* Check if destination selected is available <br>
* Sometimes, internal server error is thrown intermittently during resource creation, so please re-try

### **Unsupported Source VMs**

* VMSS as a source <br>
* AKS nodes as a source 

### **Unable to start connection Monitor**

* Check if you have the [required permissions](https://docs.microsoft.com/azure/network-watcher/required-rbac-permissions) to start a Connection Monitor. The account you log into Azure with must be assigned to either the Owner, Contributor, or Network contributor built-in roles, or assigned to a custom role that is assigned the actions listed for each Network Watcher capability. 

### **Graph not rendering**

* Check whether data is being recorded for your Connection Monitor. To verify, go to Azure Monitor >> Metrics and select your subscription, resource group, and resource type as Connection Monitors. Choose your Connection Monitor resource and metric to see is chart is generated in Azure Monitor. If chart is not generated, no data is being recorded for your Connection Monitor. In that case, check if your source VM is up, if Network Watcher extension is installed in the source VM, and if Connection Monitor topology is showing any issues for source or any other hop.

### **Monitoring data not accurate**

* Check version of your Network Watcher extension. If it is less than 1.4, reinstall the Network Watcher extension.

### **Alerts and Metrics in US Gov**

* Metrics and alerts are not be available in US Gov region 

## **Recommended Documents**

* [Connection Monitor in Azure Network Watcher](https://docs.microsoft.com/azure/network-watcher/connection-monitor)<br>
* [Permissions required to use Azure Network Watcher](https://docs.microsoft.com/azure/network-watcher/required-rbac-permissions)
