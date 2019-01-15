<properties
	pageTitle="Availability, Performance, and Application Issues/Web app experiencing high CPU"
	description="Availability, Performance, and Application Issues/Web app experiencing high CPU"
	service="microsoft.web"
	resource="sites"
	authors="shrahman, cts-shrahman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32583701"
	resourceTags=""
	productPesIds="14748,16170"
	cloudEnvironments="public"
/>

# availability, performance, and application issues/Availability, Performance, and Application Issues/Web app experiencing high CPU

## **Recommended documents**

To troubleshoot a high CPU issue, we recommend the use of the **“Diagnose and solve problems”** blade and running the CPU analysis. <br>

Here are some examples of CPU intensive operations that applications can perform. These can be resolved by avoiding these general patterns in your application: <br>
 
* Nested loops with many iterations
* Storing large collections in memory and iterating through them in each request instead of using efficient search algorithms
* Complex math operations, large string manipulations, XML transforms
* Exception handling with retries that attempt the same failing operation repeatedly
* Using large amounts of memory in your application which causes frequent page file swaps
* .NET Garbage Collection (GC) running within the application
* Running multiple CPU intensive applications on the same Application Service Plan which all compete for the same CPU resources.