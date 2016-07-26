<properties
	pageTitle="availability, performance, and application issues/http 5xx errors"
	description="availability, performance, and application issues/http 5xx errors"
	service="microsoft.web"
	resource="sites"
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32542218"
	resourceTags=""
	productPesIds="14748"
	cloudEnvironments="public"
/>

# availability, performance, and application issues/http 5xx errors

## **Recommended steps**
Assess the HTTP errors impact using Live HTTP traffic chart

1. Identify instance(s) exhibiting poor application performance (Site Metrics per Instance)
2. Attempt to resolve the issue by using Advanced Application restart
3. Identify highest CPU/Memory consuming Web app(s) within your App Service Plan (App Service plan Metrics per Instance)
4. Enable Application Logging (Filesystem)
5. Enable Failed Request Tracing

## **Recommended documents**
[Troubleshoot HTTP 5xx errors for your App](https://azure.microsoft.com/documentation/articles/app-service-web-troubleshoot-http-502-http-503/)<br>
[Remotely profile your .NET application running on App Service](https://azure.microsoft.com/blog/remote-profiling-support-in-azure-app-service/)<br>
[How to set up auto-healing](http://azure.microsoft.com/blog/2014/02/06/auto-healing-windows-azure-web-sites/)<br>
[Try Local Cache to reduce App Restarts due to Storage Failures](https://azure.microsoft.com/documentation/articles/app-service-local-cache/)<br>
[Local Cache Video](https://channel9.msdn.com/Shows/Cloud+Cover/Episode-201-Azure-Web-App-Local-Cache-with-Cory-Fowler)
