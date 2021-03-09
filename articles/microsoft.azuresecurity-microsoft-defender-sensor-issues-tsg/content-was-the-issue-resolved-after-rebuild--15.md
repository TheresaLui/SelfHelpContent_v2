<properties
	  pageTitle="Was the issue resolved after rebuild?"
	  description="Was the issue resolved after rebuild?"
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
	  articleId="5dd7f9a2-9b83-4e50-b5eb-68ed54b37ad7"
	  ownershipId="Azure_Security_Security_Center"
/>

# Was the issue resolved after rebuild?

If the log inidcates the issue 

1. Warn PerformanceCounterMetricHelper PdhAddEnglishCounter failed.
2. [pdhAddEnglishCounterResult=0xC0000BB8 SystemUpTime=23.21:28:25.1870000 FullName=\.NET CLR Memory(Microsoft.Tri.Sensor.Updater)\Promoted Memory from Gen 0 OperatingSystemFullName=\.NET CLR Memory(Microsoft.Tri.Sensor.Updater)\Promoted Memory from Gen 0]""
3. Error PerformanceCounterLib System.InvalidOperationException: Category does not exist.

For more log examples please refer to the [Wiki link](https://dev.azure.com/SupportabilityWork/Azure%20Security/_wiki/wikis/Microsoft%20Defender%20for%20Identity%20%28Azure%20ATP%29%20wiki/1780/Performance-Counter-issues?anchor=log-analysis) 

These type of logs are related to performance counter issues, it is recommended to follow the procedure below that describes how to manually rebuild Performance Counter Library values: [Rebuild Performance Counter Library values Windows Server](https://support.microsoft.com/help/300956/how-to-manually-rebuild-performance-counter-library-values) 

SE: Please share this action plan with the customer:

~~~customer
Dear Customer,

After troubleshooting the issue we found that you need to perform the following steps in order to resolve the issue:

1. Stop both MDI services
2. Rebuild counters with the following commands:
 
Rebuilding the counters, please use powershell or cmd prompt:

-cd c:\windows\system32 
-lodctr /R
-cd c:\windows\sysWOW64
-lodctr /R

3. Resyncing the counters with Windows Management Instrumentation (WMI):

WINMGMT.EXE /RESYNCPERF

4. If the above doesn't resolve the issue please reboot the affected server  

For more information [please refer to this article](https://support.microsoft.com/help/300956/how-to-manually-rebuild-performance-counter-library-values

In case you have any doubts don't hesitate to contact me.

Best Regards,

~~~

