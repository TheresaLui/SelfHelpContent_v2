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
2. If the error appears, ask customer to ensure that the perfomance counters are enabled based on the error as decribed below.
3. If the error is related to Physical disk
   1. Go to the registry key  HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\PerfDisk\Performance 
   2. [Reference](https://internal.support.services.microsoft.com/help/4514702) 
   3. You may be able to fix the PhysicalDisk error by changing the ""Disable Performance Counters"" from '1' to '0'
4. If the error is related to Network Interface : run in PowerShell > Lodctr /e:tcpip

If no graphical error appears, choose ""No"" option and continue with attempt to rebuild counters. 

