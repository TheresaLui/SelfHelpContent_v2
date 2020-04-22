<properties
pageTitle="Update management solution failed to assess at least one machine due to an HResult exception"
description="Update management solution failed to assess at least one machine due to an HResult exception"
infoBubbleText="Errors for the Update Management solution were found. See details on the right."
service="microsoft.automation"
resource="automationaccounts"
authors="katherinebecker"
ms.author="katwill"
displayOrder=""
articleId="hresultexceptions-f41aa059-0800-417d-9fe9-fc3919600a95"
diagnosticScenario="AAVmNotAssessedWithHresult"
selfHelpType="diagnostics"
supportTopicIds="32599861,32599864,32599936,32615228,32599903,32615227,32615229,32599937,32599924,32642182,32642183,32642184,32642185,32642186,32642187"
productPesIds="15607"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_Automation"
/>


# Update management solution failed to assess at least one machine due to an HResult exception

## Update management solution failed to assess at least one machine due to an HResult exception
<!--issueDescription-->
We have examined the Update Management solution on your machines and detected that while attempting to assess updates, the Windows Update Agent encountered errors on at least one machine. This indicates a problem with Windows Update configuration. This can be verified by attempting to run Windows Update manually on the impacted machines.

<!--$machinesWithHresultsTable-->[machinesWithHresultsTable]<!--/$machinesWithHresultsTable-->
<!--/issueDescription-->

## **Recommended Steps**

Review the following list of HResult exceptions for potential solutions or actions to take:
* **Exception from HRESULT: 0x……C**:
Search the relevant error code in [Windows update error code list](https://support.microsoft.com/help/938205/windows-update-error-code-list) to find additional details on the cause of the exception
* **0x8024402C**, **0x8024401C**, **0x8024402F**:
  These errors are network connectivity issues. Make sure that your machine has the proper network connectivity to Update Management. See the section on [network planning](https://docs.microsoft.com/azure/automation/automation-update-management#ports) for a list of ports and addresses that are required.
* **0x8024001E**:
  The update operation did not complete because the service or system was shutting down
* **0x8024002E**: 
  Windows Update service is disabled
* **0x8024402C**:  
  If you are using a WSUS server, make sure the registry values for WUServer and WUStatusServer under the registry key HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate have the correct WSUS server
* **0x80072EE2**:
  Network connectivity issue or issue talking to a configured WSUS server. Check WSUS settings and make sure it is accessible from the client.
* **The service cannot be started, either because it is disabled or because it has no enabled devices associated with it. (Exception from HRESULT: 0x80070422)**:
  Make sure the Windows Update service (wuauserv) is running and is not disabled
* For any other generic exception, do a search the internet for the possible solutions and work with your local IT support

If the above list doesn’t include the HResult from your machine, please check the below documentation link for the latest list of HResults.

## **Recommended Documents**

* [Troubleshooting HResult exceptions](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult)
