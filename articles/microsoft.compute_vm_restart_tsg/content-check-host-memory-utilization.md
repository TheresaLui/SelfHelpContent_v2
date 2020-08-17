<properties
	pageTitle="Check host memory issues"
	description="Check host memory issues"
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
	articleId="f16ee7ae-6caf-48c1-8045-52a6f032762d"
   ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check host memory issues

If the available memory left for the host node drops below 2048 MB (older Node Generations) or below 6196 MB (newer Node Generations) we may face a potential host node issue.

**Check using Hostanalyzer**

To see VM allocation failures due to low memory condition, look on the host on Hostanalyzer tab "Host Metrics/Host Charts". The chart will show host memory available in MBytes.

**Use kusto to investigate memory resource exhaustion**

[Kusto query for memory resource exhaustion](https://vmainsight.kusto.windows.net/vmadb )

~~~kusto 

WindowsEventTable
| where EventId == "2004" and ProviderName contains "Microsoft-Windows-Resource-Exhaustion-Detector"
| where NodeId == "<NodeID>"
| where PreciseTimeStamp >  datetime(<StartTime>)
| where PreciseTimeStamp < datetime(<EndTime>)

~~~

This low memory condition could result into a VM restart (RCA to be used):
https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD?wikiVersion=GBmaster&pagePath=%2FGeneralPages%2FAzure%2FAzure_Virtual%20Machine_Restart_RCA_Nodefault%20%252D%20low%20memory

**Use kusto to investigate if low memory is preventing a VM from starting**

[Kusto query for failed to start VM](https://vmainsight.kusto.windows.net/vmadb )

~~~kusto

WindowsEventTable 
| where EventId in ("12030","3122","3050","2004") and ProviderName contains "Microsoft-Windows-Hyper-V-Worker"
| where NodeId == "<NodeID>"
| where PreciseTimeStamp >  datetime(<StartTime>)
| where PreciseTimeStamp < datetime(<EndTime>)

~~~

Possible event IDs for low memory preventing VM start

|Eventid|Provider|Channel|Message or Context|
|-|-|-|-|
|2004|Microsoft-Windows-Resource-Exhaustion-Detector|System|"Windows successfully diagnosed a low virtual memory condition. The following programs consumed the most virtual memory: …"|
|3122|Microsoft-Windows-Hyper-V-Worker|System|"Not enough memory in the system to start the virtual machine…"|
|3050|Microsoft-Windows-Hyper-V-Worker|System|<guid of container> could not initialize memory: Ran out of memory (0x8007000E)..."|
|12030|Microsoft-Windows-Hyper-V-Worker|Microsoft-Windows-Hyper-V-Worker-Admin|<guid of container> failed to start. (Virtual machine ID <guid>)|

**Use kusto determine if there's not enough system memory**

By using Table [TMMgmtTenantEventsEtwTable in Kusto](https://azurecm.kusto.windows.net/AzureCM?query=H4sIAAAAAAAEAH3PwQqCQBgE4HvgO%2Fx4KmhhVw3dyG4ejaB9gVUHM1oT9ycvPXxCRIcimMswfIcxZdk6Nuhtz8UdPfuCJ2OrK4LFg6YzRtBrPVgHynMK40irWNlKpBsJkaQKIkt1JlSjtZJI0NRx%2BNHHEXXnYTqHE1s30J4ay%2BC5LyOptJBzEorkVsrVH7b7zdSbDePtgpq%2F4JpKeG%2Fb%2BVCweAJnyX%2B07wAAAA%3D%3D&web=0)


~~~kusto

TMMgmtTenantEventsEtwTable
| where TenantName == "<tenantName>"
| where PreciseTimeStamp > datetime(<Starttime>)
| where PreciseTimeStamp < datetime(<EndTime>)
| project PreciseTimeStamp, Message

~~~

We would see VM fails to starts and gets service healed multiple times via this example error message: Service Healing Trigger. Type:Container
Not enough memory in the system to start the virtual machine <tenantName> with ram size x megabytes. (Virtual machine ID <vmid>)
'<tenantName>' could not initialize memory: Ran out of memory (0x8007000E).

You can also look for status code "0xc153000b" and "VMAL_E_IVM_START_FAILED" on TMMgmtTenantEventsEtwTable in combination with low available memory on host node using Hostanalyzer.

**Check if the issue is related on low memory on Gen3 Nodes leading to missing disk**

Kusto query for low Memory on Gen3 Nodes lead to disk missing on DS14

~~~kusto

WindowsEventTable 
| where NodeId == "<nodeid>" 
| where PreciseTimeStamp >= datetime(<StartTime>) and PreciseTimeStamp <= datetime(<EndTime>)
| where EventId == 2
| where ProviderName == "VhdDiskPrt"
| where Description contains "C0000017"
| project TimeCreated, EventId, ProviderName, Description

~~~

Lookup error code "C0000017" on [internal website](http://errors/)

0xc0000017 STATUS_NO_MEMORY {Not Enough Quota} Not enough virtual memory or paging file quota is available to complete the specified operation. ntstatus.h

**Investigate memory related hardware failures**

The following EventIDs could point to memory related hardware issues (some events need to be logged multiple times to be more conclusive)

|Eventid|Provider|Channel|Message|Context|
|-|-|-|-|-|
|16;40|Microsoft-Windows-WHEA-Logger|System|A fatal hardware error has occurred. Component: PCI Express Root Port Error Source: Generic Bus:Device:Function: 0x81:0x0:0x0 Vendor ID:Device ID: 0x9005:0x28D Class Code: 0x104 The details view of this entry contains further information.|Memory error (PCIeErrorUncorrected)|
|17;41|Microsoft-Windows-WHEA-Logger|System|A corrected hardware error has occurred. Component: PCI Express Root Port Error Source: Generic Bus:Device:Function: 0x9E:0x0:0x0 Vendor ID:Device ID: 0x144D:0xA804 Class Code: 0x108 The details view of this entry contains further information.|Memory error (PCIeErrorCorrected)|
|22;46|Microsoft-Windows-WHEA-Logger|System|A fatal hardware error has occurred. Component: Memory Error Source: BOOT Error Type: Multi-Bit ECC The details view of this entry contains further information.|Memory error (MemoryErrorUncorrected)|
|23;47|Microsoft-Windows-WHEA-Logger|System|A corrected hardware error has occurred. Component: Memory Error Source: Generic Error Type: Single-Bit ECC The details view of this entry contains further information.|Memory error (MemoryErrorCorrected)|

**Check for hardware issues due to ECC errors**

Kusto query for SEL log analysis

union
(cluster("Azuredcm").database("AzureDCMDb").RhwBmcSelItemEtwTableV1   | extend SelSource = "RhwBmcSelItemEtwTableV1"    ),
(cluster("Azuredcm").database("AzureDCMDb").RhwChassisSelItemEtwTable | extend SelSource = "RhwChassisSelItemEtwTable"  ),
(cluster("Azuredcm").database("AzureDCMDb").RhLiteDiagBmcSel          | extend SelSource = "RhLiteDiagBmcSel"           ),
(cluster("Azuredcm").database("AzureDCMDb").RhLiteDiagSel             | extend SelSource = "RhLiteDiagSel" | extend BmcSelItemTimeStamp= SelTimeStamp)
| where BmcSelItemTimeStamp between (datetime(<StartTime>) .. datetime(<EndTime>))
| where ResourceId in ("<NodeId>")
| where BmcSelItemEventType != "CollectoreHeartbeat"
| project-away TIMESTAMP, PreciseTimeStamp, Tenant, Lens_IngestionTime, Lens_Originator, Lens_OriginatorData, Lens_SessionId, Lens_BatchId, Lens_JobId
| extend HasHex = isnotempty(BmcSelItemRawHex) 
| extend MissingHex = isempty(BmcSelItemRawHex)

If you find more than 10 Correctable ECC errors (logging usually stopped by "Event Logging Disabled; Assert: Correctable Memory Error") and/or an Uncorrectable ECC this is pointing to memory related hardware failure 