<properties
	pageTitle="Availability, performance, and application issues/problems with webjobs"
	description="Availability, performance, and application issues/problems with webjobs"
	service="microsoft.web"
	resource="sites"
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32542219"
	resourceTags=""
	productPesIds="14748"
	cloudEnvironments="public"
/>

# availability, performance, and application issues/problems with webjobs
## **Recommended steps**

1. For scheduled WebJobs to work correctly the website needs to be configured as Always On. For more information, please check the Wiki link below. 
2. To see the scheduler logs for a scheduled WebJob you need to use the get triggered WebJob api, go to the url: https://{sitename}.scm.azurewebsites.net/api/triggeredwebjobs/{jobname} (remove the job name to see all triggered WebJobs).
3. It is possible to run WebJobs when the Web App is stopped.  If it runs on a schedule, it will continue to run based on that schedule until the WebJob is deleted or disabled using WEBJOBS_STOPPED, regardless of the state of the Web App.

## **Recommended documents**
[WebJobs Wiki](https://github.com/projectkudu/kudu/wiki/Web-jobs)<br>
[List of WebJobs Resources](https://azure.microsoft.com/documentation/articles/websites-webjobs-resources/)
