<properties
	pageTitle="Availability, Performance, and Application Issues/Web app experiencing high CPU"
	description="Availability, Performance, and Application Issues/Web app experiencing high CPU"
	service="microsoft.web"
	resource="sites"
	authors="cts-shrahman, cts-shrahman"
    ms.author="shrahman,toan"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32583701"
	resourceTags=""
	productPesIds="16170,16333"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="e069f1f0-c8f7-49bb-85e0-e5969545e59e"
	ownershipId="Compute_AppService"
/>

# availability, performance, and application issues/Availability, Performance, and Application Issues/Web app experiencing high CPU

## **Recommended Steps**

Here are some examples of CPU intensive operations that applications can perform. These can be resolved by avoiding these general patterns in your application: <br>

* Nested loops with many iterations <br>
* Storing large collections in memory and iterating through them in each request instead of using efficient search algorithms <br>
* Complex math operations, large string manipulations, XML transforms <br>
* Exception handling with retries that attempt the same failing operation repeatedly <br>
* Using large amounts of memory in your application which causes frequent page file swaps <br>
* .NET Garbage Collection (GC) running within the application <br>
* Running multiple CPU intensive applications on the same Application Service Plan which all compete for the same CPU resources 

## **Recommended Documents**

* [Monitor, diagnose and troubleshoot performance issues](https://docs.microsoft.com/azure/app-service/troubleshoot-performance-degradation)
* [Finding Memory Leaks and CPU Usage in Azure Node.js Web App](https://azureossd.github.io/2015/08/23/finding-memory-leaks-and-cpu-usage-in-azure-node-js-web-app/)
* [Troubleshoot HTTP 502 or 503 errors for your Web App](https://docs.microsoft.com/azure/app-service/troubleshoot-http-502-http-503)
* [10 Ways to Speed up your WordPress site on Azure Web App](https://azure.microsoft.com/blog/10-ways-to-speed-up-your-wordpress-site-on-azure-websites/)
* [WordPress Scheduled Jobs (wp-cron.php) and Slowness][https://azureossd.github.io/2015/06/11/wordpress-scheduled-jobs-wp-cron-php-and-slowness/]
* [Application Monitoring and Performance Management with Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview)
