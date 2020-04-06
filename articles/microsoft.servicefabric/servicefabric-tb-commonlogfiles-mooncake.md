<properties 
    pageTitle="Common log files for Service Fabric nodes" 
    description="Common log files for Service Fabric nodes" 
    service="microsoft.servicefabric"
    resource="clusters"
    authors="pkcsf"
    ms.author="pkc"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servicefabric"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="311ce7f1-1008-4f9e-a95c-de343221a8fb"
	ownershipId="Compute_ServiceFabric"
/>

# Common log files for Service Fabric nodes

## **Recommended Steps**

You can easily capture all of the most common log files from a Service Fabric node with a single command. This will create a ZIP file that you can then save offline for post-mortem analysis. To create the ZIP file, [RDP](https://docs.azure.cn/service-fabric/service-fabric-cluster-nodetypes/#remote-connect-to-a-vm-scale-set-instance-or-a-cluster-node) to a node and run `CollectGuestLogs.exe`.  CollectGuestLogs.exe can be found in the Azure Guest Agent folder (C:\WindowsAzure\GuestAgent_x.x.xxxxx.xxx\CollectGuestLogs.exe). Among the files collected, these are most commonly used to troubleshoot problems:

* Event Logs
    * Service Fabric Event Logs
    * Application and System Event Logs
    * Azure Event Logs
* Azure Guest Agent logs
* Extension/Plugin Setup Logs and Status Blobs
* Node configuration
* Service Fabric Installation Logs
* Windows Azure Diagnostics logs and cached data

## **Recommended Documents**

* [Monitor and diagnose services in a local machine development setup](https://docs.azure.cn/service-fabric/service-fabric-diagnostics-how-to-monitor-and-diagnose-services-locally/) for how to configure ETW traces in your application
* [Debug your Service Fabric application by using Visual Studio](https://docs.azure.cn/service-fabric/service-fabric-debugging-your-application/) for how to use Visual Studio to debug and view ETW traces for a remote Service Fabric app
