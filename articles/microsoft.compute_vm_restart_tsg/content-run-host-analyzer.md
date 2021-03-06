<properties
	pageTitle="How to run host analyzer"
	description="How to run host analyzer"
	service="microsoft.compute"
	resource="Microsoft.Compute/virtualMachines"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="83e7dc12-93dc-4aa9-8826-4925777d3db7"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to run host analyzer

Host Analyzer is a one stop tool which captures details from a Host Node perspective and provides you with a holistic view of what was going on the Host during the specified time. This tool should be run in scenarios where you suspect the Host Node has issues.

1. Under the Resource Explorer, select the Virtual Machine customer informed felt unavailability.
2. Navigate to the Health tab.
3. Select the day around the timeframe of the issue and click the "Run" button.
4. Go to section Container Change Events to get the sets of Cluster, Node Id and Container Id at the occurrence time of the issue.
5. Save the data for next steps.
6. Navigate to Host Analyzer section on Diagnostics tab.
7. Click in create report and add the information you saved from steps 4 and 5.
8. For the Start Time and Stop Time, make sure you provide a time windows of 2-3 hours around the time of the issue.
9. Click on “Run”.

**General Findings**
This gives a consolidated view of the findings on the Node during the time specified. Some of the details it provides:
   1. BugCheck happened on the Node.
   2. Node Reboots.
   3. Throttling on disks.
   4. Network connectivity drops.

**VM Metrics**
1. **VM BlobPerf** – This provides the details with respect to XIOPS, NWIOPS, latency, IO retries, IOs throttled and IO trim bytes with a timestamp. You can look the exact time when large IOs were throttled or IO bytes were trimmed.
2. **VM Limit Charts** – This provides graphical representation of VM CPU performance, latency, IO failures, IOPs etc. This way you can easily figure out if the VM is having high CPU consistently or if there were a high number of IOs throttled.
For more understanding of the HostAnalyzer Charts, go through the training uploaded here  
3. **Blob Perf Charts** – This provides graphical representation of blob performance charts.
4. **Blobs** - This provides the BlobPath, its CachingPolicy and if the Disk is a part of Standard or Premium Storage. If the IsXIOdisk value is 0, then it is a standard disk, if the value is 1, then it’s a premium storage.

**Host Metrics**
This again provides the graphical representation of the Host performance during the time, providing details about the CPU, Memory etc. For more understanding of the HostAnalyzer Charts, go through the [training uploaded here](https://microsoft.sharepoint.com/teams/AzureSupportability/Shared%20Documents/SPM/Operational%20Supportability/Diagnostics%20Scenarios/Diagnostic/Host%20Analzer%20and%20GetSub%20Brownbag%20AM%20PST.mp4).

**Events**
This provides the consolidated view of the Host Event Logs. Check for any Event ID 2, Event ID 3 preceding the Event 17 while troubleshooting XStore issues.

**Network**
Check the PingMesh Availability for any network issues. If the availability falls below 1, then it can be inferred that there were network related issues. Engage CloudNet team via CRI for further investigation.