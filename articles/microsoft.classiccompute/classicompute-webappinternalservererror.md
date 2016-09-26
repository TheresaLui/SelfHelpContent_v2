<properties 
	pageTitle="My web application shows Internal Server Error or Service Unavailable (50x)"
	description="My web application shows Internal Server Error or Service Unavailable (50x)"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="jluk"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	 
	productPesIds=""
	cloudEnvironments="public"
/>

# My web application shows Internal Server Error or Service Unavailable (50x)

## **Recommended steps**
These errors are treated as application errors, so you should troubleshoot them like any on premise hosted application.  

1.	Remote into the instances and check that you can access the web application locally. <br> 
This will determine if the issue is only encountered on some of the instances, or all instances.

2.	Review the IIS logs for the specific failed request (50x). <br>
The logs are generally located at *C:\Resources\Directory\guid.role.DiagnosticStore\LogFiles\W3SVC1*.

3.	Review the **Application Logs** in **Event Viewer** on the same instance with failed request; look for more details about the HTTP **50x** error.

4.	Add extra logging to your application.<br>

5.  Put a **helloworld.html** test file into the **sitesroot** folder. <br>
If any startup files like **global.asax** or **web.config** have problems, then accessing **helloworld.html** will have the same issue. This will help determine that the problem is related to the website itself.

6.  Enable **Failed Request Tracing** in **IIS** to see the detailed error message.

7.	Use **DebugView** to capture exceptions/errors.

8.	For further diagnostics, use **[DebugDiag](https://msdn.microsoft.com/library/ff420662.aspx)**, **ProcDump** or **WinDbg** to capture and review memory dumps. This will give pointers where the problem is.
