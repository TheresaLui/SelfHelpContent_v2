<properties
	  pageTitle="Did the action plan helped resolve the Perfmon errors?"
	  description="Did the action plan helped resolve the Perfmon errors?"
      service="Microsoft.Security"
      resource="Microsoft.Security/assessments"
	  authors="rimayber"
	  ms.author="rimayber"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="202554bb-5f35-4d6d-914c-a5632706a90b"
	  ownershipId="Azure_Security_Security_Center"
/>

# Did the action plan helped resolve the Perfmon errors?

1. Open performance monitor and check if a graphical error appears:  **Unable to Add these counters**
    1. Error examples: \\Memory\AvailableMbytes or \\PhysicalDisk(*)\Idle Time
2. If the error appears, ask customer to ensure that the perfomance counters are enabled based on the error as decribed below. Please share the action plan with the customer. A sample customer ready message is provided below. 

If no graphical error appears, please check in the logs which type of Performance Counter is affected and in case there are none specified follow the procedure related to the Network Interface.
The procedure is available in the WIKI: [Performance Counter issues](https://dev.azure.com/SupportabilityWork/Azure%20Security/_wiki/wikis/Microsoft%20Defender%20for%20Identity%20%28Azure%20ATP%29%20wiki/1780/Performance-Counter-issues)

~~~customer

Dear Customer:

After troubleshooting the issue we found that you need to check for the error and proceed with the solution below:

1. Check for **DisablePerformanceCounters** regkey, they should not exist or be set to “0”:

HKLM\System\CurrentControlSet\Services\PerfOS\Performance
HKLM\System\CurrentControlSet\Services\PerfProc\Performance\
HKLM\System\CurrentControlSet\Services\PerfNet\Performance\

Best regards,

~~~