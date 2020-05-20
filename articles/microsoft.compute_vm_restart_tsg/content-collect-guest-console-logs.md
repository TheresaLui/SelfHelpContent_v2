<properties
	pageTitle="How to collect guest and console logs"
	description="How to collect guest and console logs"
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
	articleId="7cac27f4-b4a8-4591-aac4-34783cab1318"
   ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to collect guest and console logs

1. You can collect the screenshot image of the affected VM from Hyper-V layer in the fabric through ASC.
   1. Navigate to the Diagnostics tab under Resource Explorer in ASC and see the Screenshot section.
   2. Push + button and then the screenshot at the point will be created. You can get the current screen image of the affected VM. 
2. How to get Host Analyzer logs for the unavailable event of customer VM in ASC
   1. Navigate to Health tab in ASC for the VM
   2. Select the day around the time frame of the issue and click the "Run" button.
   3. Go to section Container Change Events to get the sets of Cluster, Node Id and Container Id at the occurrence time of the issue **Note:** The ContainerChangeEvents info will be shown only at the point when a container was generated. You will need that time to use on HostAnalyzer by setting the period from at least 30 minutes before the issue occurred to the time after 1 hour. (having in mind the timespan that the issue happened).

   4. Navigate to Host Analyzer section on Diagnostics tab in ASC. If you need to run Host Analyzer other than the one initially created, for example, it doesn't match the target node or period, please initiate a manual run by providing a 2-3 hour time window around the time of the issue, Cluster, Node Id and Container Id at the time of the issue (optional fields need to be filled).
3. How to get Guest OS logs in ASC. **Note:** If customer disks are encrypted, it will fail with error. The guest OS logs need to be collected by the customer by uploading necessary logs to DTM share (no other option possible as of now).
   1. For Windows
      1. To collect Guest OS logs for Windows VMs, under ASC you need to follow the next steps
      2. Go Diagnostics tab under Resource Explorer in ASC.
      3. Search for Inspect IaaS Disk section and select + Create Report
      4. Select the Diagnostic Mode and select the checkbox to Run WinGuest Analyzer and provide the start and end time around the time of the issue: **Note:** We sometimes call it IID (Inspect IaaS Disk) log. If you specify the flag of Run WinGuest Analyzer, it will automatically analyze the Guest OS logs and produce the report. This report will be shown as another link and have some insights and formatted logs with hyper-text.
   2. For Linux. To collect Guest OS logs for Linux VMs, under ASC you need to follow the next steps
      1. Go Diagnostics tab under Resource Explorer in ASC.
      2. Search for Serial Console.
      3. If it is already generated before you collect manually, you can use it. In some situations, the initially collected console log might be more useful than the newest one. For example, talking about a crash event, if the console log was collected before the machine was not stopped/deallocated or redeployed, that console log will have the information about the issue happening at the crash time. Once the customer deallocates(redeploys)/restarts the affected VM, the console log will be recreated.
      4. If none is generated, click Get current console log button
      5. Then create a InspectIaaS Disk report by selecting + Create Report. Choose the Normal and provide the start and end time around the time of the issue:
