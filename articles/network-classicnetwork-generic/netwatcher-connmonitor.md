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
	cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
	articleId="67d46e6c-ee76-4433-8e11-1adcbdef0e12"
	ownershipId="CloudNet_NetAnalytics"
/>

# Connection Monitor

## **Recommended Steps**

### **Internal Server Error while trying to create Connection Monitor**

* Check if Network Watcher is installed in the region you are trying to create Connection Monitor in. [Use this link to install Network Watcher in a region](https://docs.microsoft.com/azure/network-watcher/network-watcher-create).
* Check if Network Watcher is supported in the region you are trying to create Connection Monitor in <br>
* Ensure that your source VM has Network Watcher extension installed without issues and is in the same subscription in which you are trying to create the Connection Monitor <br>
* Check if destination selected is available <br>
* Sometimes an internal server error is thrown intermittently during resource creation, so please retry

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

* Metrics and alerts are now be available in US Gov region 

## **Connection Monitor (Preview) - Recommended Steps**

### **Unable to see my Azure VM in the list of sources**

* Your Azure VM needs to be in the same subscription and region as the Connection Monitor you are trying to create
* Check if Network Watcher extension is installed in the Azure VM.
* Check if you have access to the VM

### **Unable to see my on-premise host in the list of sources**

* Check if Log Analytics agent is installed in your on-premise host, is linked to a Log Analytics workspace and that you have access to the workspace

### **Unable to see my Azure VM in the list of destinations**

* Check if you have chosen on-premise host as a source in your test group. The ability for on-premise hosts to ping Azure VMs is currently not available. 

### **Can I customize the workspace in which I want to store network monitoring data**

* You can provide the custom workspace by unchecking "Use workspace created by connection monitor(default)". Just select the subscription and region to see the workspaces that you have access to in the list.

### **What is a connection monitor, test group and test**

* Connection Monitor Resource – Region specific Azure resource. All the entities mentioned below are properties of a Connection Monitor resource.
* Endpoints – All sources and destinations that participate in connectivity checks are called as endpoints. Examples of endpoint – Azure VMs, On Premise agents, URLs, IPs.
* Test Configuration – Each test configuration is protocol specific. Based on the protocol chosen, you can define port, thresholds, test frequency and other parameters.
* Test Group – Each test group contains source endpoints, destination endpoints and test configurations. Each Connection Monitor can contain more than one test groups.
* Test – Combination of a source endpoint, destination endpoint and test configuration make one test. This is the lowest level at which monitoring data (checks failed % and RTT) is available.

### **Is Powershell/CLI available for Connection Monitor(Preview)**

* Yes, you can use powershell and CLI to create / update Connection Monitor

### **Does Connection Monitor(Preview)support IPv6**

* Yes, Connection Monitor(Preview) supports IPv6

### **How is Checks Failed % calculated for a test**
* If HTTP is selected, the service calculates the number of HTTP responses that returned a response code to determine the checks failed %.  To calculate RTT we measure the time taken to receive the response of a HTTP call. 
* If TCP or ICMP is selected, the service calculates packet % to determine checks failed %. To calculate RTT we measure the time taken to receive the ACK for packets sent. If you have enabled traceroute data for your network tests, you will be able to hop-by-hop loss and latency for your on-premise network.


### **Unsupported Source VMs**

* VMSS as a source <br>
* AKS nodes as a source 

### **Unable to start connection Monitor**

* Check if you have the [required permissions](https://docs.microsoft.com/azure/network-watcher/required-rbac-permissions) to start a Connection Monitor. The account you log into Azure with must be assigned to either the Owner, Contributor, or Network contributor built-in roles, or assigned to a custom role that is assigned the actions listed for each Network Watcher capability. 

### **Graph not rendering**

* Check whether data is being recorded for your Connection Monitor. To verify, go to Azure Monitor >> Metrics and select your subscription, resource group, and resource type as Connection Monitors. Choose your Connection Monitor resource and metric to see is chart is generated in Azure Monitor. If chart is not generated, no data is being recorded for your Connection Monitor. In that case, check if your source VM is up, if Network Watcher extension is installed in the source VM, and if Connection Monitor topology is showing any issues for source or any other hop.

### **Monitoring data not accurate**

* Check version of your Network Watcher extension. If it is less than 1.4, reinstall the Network Watcher extension.

### **Deleted Connection Monitor still showing up in the dashboard**

* The dashboard loads data for a time duration in the UI, hence the Connection Monitor might be showing up. This should disappear in about 5 minutes

## **Recommended Documents**

* [Connection Monitor in Azure Network Watcher](https://docs.microsoft.com/azure/network-watcher/connection-monitor)<br>
* [Connection Monitor (Preview) in Azure Network Watcher](https://docs.microsoft.com/azure/network-watcher/connection-monitor-preview)<br>
* [Permissions required to use Azure Network Watcher](https://docs.microsoft.com/azure/network-watcher/required-rbac-permissions)
