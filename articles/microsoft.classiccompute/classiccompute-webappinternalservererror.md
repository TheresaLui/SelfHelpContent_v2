<properties 
	pageTitle="My web application shows Internal Server Error or Service Unavailable (50x)"
	description="My web application shows Internal Server Error or Service Unavailable (50x)"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="jluk"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	 
	productPesIds=""
	cloudEnvironments="public, fairfax, MoonCake, usnat, ussec"
	articleId="bf86ef14-68e0-4fb9-a314-0f2f7541296e"
	ownershipId="Compute_VirtualMachines"
/>

# My web application shows Internal Server Error or Service Unavailable (50x)
These errors are treated as application errors, so you should troubleshoot them like any on premise hosted application.  

## **Recommended steps**

1.	Remote into the instances and check that you can access the web application locally. <br> 
By checking locally, you can investigate and determine if the issue is only encountered on some, or all, of the instances.

2.	Review the IIS logs for the specific failed request (50x). <br>
The logs are generally located at *C:\Resources\Directory\guid.role.DiagnosticStore\LogFiles\W3SVC1*.

3.	Review the **Application Logs** in **Event Viewer** on the same instance with failed request; look for more details about the HTTP **50x** error.

4.	Add extra logging to your application.<br>

5.  Put a **helloworld.html** test file into the **sitesroot** folder. <br>
If any startup files (like **global.asax** or **web.config**) have problems, then accessing **helloworld.html** will have the same problem. This helps determine that the problem is related to the website itself.

6.  Enable **Failed Request Tracing** in **IIS** to see the detailed error message.

7.	Use **DebugView** to capture exceptions/errors.

8.	For further diagnostics, use **[DebugDiag](https://msdn.microsoft.com/library/ff420662.aspx)**, **ProcDump**, or **WinDbg** to capture and review memory dumps. This gives pointers where the problem is.
