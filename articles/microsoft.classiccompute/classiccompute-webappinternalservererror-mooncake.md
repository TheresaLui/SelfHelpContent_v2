<properties 
	pageTitle="My web application shows Internal Server Error or Service Unavailable (50x)"
	description="My web application shows Internal Server Error or Service Unavailable (50x)"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="jluk"
	ms.author="juluk"
	displayOrder="30"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	 
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="classiccompute-webappinternalservererror-mooncake"
	ownershipId="Compute_VirtualMachines"
/>

# My web application shows Internal Server Error or Service Unavailable (50x)

These errors are treated as application errors, so you should troubleshoot them like any on-premise hosted application.  

## **Recommended Steps**

* Rte into the instances and check that you can access the web application locally. By checking locally, you can investigate and determine if the issue is only encountered on some, or all, of the instances.
* Review the IIS logs for the specific failed request (50x). The logs are generally located at *C:\Resources\Directory\guid.role.DiagnosticStore\LogFiles\W3SVC1*.
* Review the **Application Logs** in **Event Viewer** on the same instance with failed request; look for more details about the HTTP **50x** error
* Add extra logging to your application
* Put a **helloworld.html** test file into the **sitesroot** folder. If any startup files (like **global.asax** or **web.config**) have problems, then accessing **helloworld.html** will have the same problem. This helps determine that the problem is related to the website itself.
* Enable **Failed Request Tracing** in **IIS** to see the detailed error message
* Use **DebugView** to capture exceptions/errors
* For further diagnostics, use **DebugDiag**, **ProcDump**, or **WinDbg** to capture and review memory dumps. This gives pointers where the problem is.
