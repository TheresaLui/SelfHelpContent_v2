<properties
	pageTitle="Availability, Performance, and Application Issues/Web app experiencing high CPU"
	description="Availability, Performance, and Application Issues/Web app experiencing high CPU"
	service="microsoft.web"
	resource="sites"
	authors="cts-shrahman, cts-shrahman"
    ms.author="shrahman,shrahman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32583701"
	resourceTags=""
	productPesIds="14748"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="abbda638-0267-4223-b95b-f35e9a35dde1"
	ownershipId="Compute_AppService"
/>

# availability, performance, and application issues/Availability, Performance, and Application Issues/Web app experiencing high CPU

## **Recommended Steps**

To troubleshoot a high CPU issue, we recommend the use of the **"Diagnose and solve problems"** blade and running the High CPU analysis.

Watch these videos to learn more about troubleshooting High CPU Issues in Azure App Service
* [How to identify and diagnose apps with high CPU: Part 1 - Azure App Service](https://youtu.be/tavdGmIX0xg)
* [How to identify and diagnose apps with high CPU: Part 1 - Azure App Service](https://youtu.be/2kewsEVn9I4)

Here are some examples of CPU intensive operations that applications can perform. These can be resolved by avoiding these general patterns in your application: 
 
* Nested loops with many iterations <br>
* Storing large collections in memory and iterating through them in each request instead of using efficient search algorithms <br>
* Complex math operations, large string manipulations, XML transforms <br>
* Exception handling with retries that attempt the same failing operation repeatedly <br>
* Using large amounts of memory in your application which causes frequent page file swaps <br>
* .NET Garbage Collection (GC) running within the application <br>
* Running multiple CPU intensive applications on the same Application Service Plan which all compete for the same CPU resources 
