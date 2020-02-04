<properties
  pageTitle="networkwatcher/connectionmonitorpreview"
  description="networkwatcher/connectionmonitorpreview"
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
	articleId="67d46e6c-ee76-4433-8e11-1afcbdef0e12"
/>

# Connection Monitor (Preview)

## **Recommended Steps**

### **Unable to see my Azure VM in the list of sources**

* Your Azure VM needs to be in the same subscription and region as the Connection Monitor you are trying to create
* Check if Network Watcher extension is installed in the Azure VM.
* Check if you have access to the VM

### **Unable to see my on-premise host in the list of sources**

* Check if Log Analytics agent is installed in your on-premise host, is linked to a Log Analytics workspace and thatyou have access to the workspace

### **Unable to see my Azure VM in the list of destnations**

* Check if you have chosen on-premise host as a source in your test group. The baility for on-premise hosts to ping Azure VMs is currently not available. 

### **Can I customise the workspace in which I want to sendmy monitoring data**

* You can provide the custom workspace by unchecking "Use workspace created by connection monitor(default)". Just select the subscription and region to see the workspaces that you have access to in the list.

### **What is a connection monitor, test group and test**

* Connection Monitor Resource – Region specific Azure resource. All the entities mentioned below are properties of a Connection Monitor resource.
* Endpoints – All sources and destinations that participate in connectivity checks are called as endpoints. Examples of endpoint – Azure VMs, On Premise agents, URLs, IPs 
* Test Configuration – Each test configuration is protocol specific. Based on the protocol chosen, you can define port, thresholds, test frequency and other parameters
* Test Group – Each test group contains source endpoints, destination endpoints and test configurations. Each Connection Monitor can contain more than one test groups
* Test – Combination of a source endpoint, destination endpoint and test configuration make one test. This is the lowest level at which monitoring data (checks failed % and RTT) is available

### **Is Powershell/CLI available for Connection Monitor(Preview)**

* Yes you can use powershell and CLI to create / update Connection Monitor

### **Does Connection Monitor(Preview)support IPv6**We are having facing limited flexibility and overview of the current NPM solution. For example you can’t label subnets so you can easily see which IP ranges correspond with what subnet in the subnet status overview, auto-refresh behaviour unpredictable, little flexibility changing graph time range, no option to change Y scale, no manual threshold for “health Events” (it happens often that when you open the dashboard the status is red but after reresh it is fine because of small hickups), error messages when you are not contributor when new objects were found, etc. NPM just looks very old compared with the new Azure Monitor graphs. To summarize: the overall user experience is pretty lacking and we would love to see a new incarnation of it!  

* Yes Connection Monitor(Preview) support IPv6**

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

* The dashboard loads data for a time duration in the UI, hence the Connection Monitor might be showing up.This should disappear in about 5 minutes

## **Recommended Documents**

* [Connection Monitor in Azure Network Watcher](https://docs.microsoft.com/azure/network-watcher/connection-monitor-preview)<br>
* [Permissions required to use Azure Network Watcher](https://docs.microsoft.com/azure/network-watcher/required-rbac-permissions)
