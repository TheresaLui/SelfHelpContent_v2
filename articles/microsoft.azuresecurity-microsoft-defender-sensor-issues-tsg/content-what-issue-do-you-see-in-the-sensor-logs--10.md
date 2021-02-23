<properties
	  pageTitle="What issue do you see in the sensor logs?"
	  description="What issue do you see in the sensor logs?"
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
	  articleId="2822cac7-d9ce-4352-907e-e29e64322919"
	  ownershipId="Azure_Security_Security_Center"
/>

# What issue do you see in the sensor logs?

Collect the sensor logs and analyse the issue.
Sensor logs usually located in: ?C:\Program Files\Azure Advanced Threat Protection Sensor\version number\Logs?

Microsoft.Tri.Sensor.log
Microsoft.Tri.Sensor-Errors.log
Microsoft.Tri.Sensor.Updater.log

Common issues can be:
1. Directory Services Connectivity
2. Performance Counter, log would indicate: "Warn  PerformanceCounterMetricHelper PdhAddEnglishCounter failed."
3. Connectivity issues
4. Directory connectivity > GMSA and Account

If the customer hasn't provided sensor logs, please use the customer ready message below to ask the customer for sensors logs

~~~customer

Could you please upload the following log files in order to analyze the issue.

Sensor logs are usually located in: C:\Program Files\Azure Advanced Threat Protection Sensor\version number\Logs

Microsoft.Tri.Sensor.log
Microsoft.Tri.Sensor-Errors.log
Microsoft.Tri.Sensor.Updater.log

Best Regards,

~~~