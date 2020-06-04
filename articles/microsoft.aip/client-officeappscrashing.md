<properties
	pageTitle="Azure Information Client - Office apps are crashing"
	description="Azure Information Client - Office apps are crashing"
	service="microsoft.aip"
	resource="aip"
	authors="nihendle"
	ms.author="nihendle, orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584359"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="75b5c7b4-12c4-4576-808d-0e8c75efe70b"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection client - Office apps are crashing

## **Recommended Steps**

1. Disable all enabled add-ins except **Microsoft Azure Information Protection**, and verify if the issue persists
2. If the issue does not reproduce after disabling add-ins, enable them one by one to identify which one create the add-in clash
3. Temporarily disable all security products that are running, especially anti-virus services, and verify if the issue persists
4. Verify that your Office suite is updated to the latest version
5. Verify the [firewall and network requirements](https://docs.microsoft.com/azure/information-protection/get-started/requirements#firewalls-and-network-infrastructure) for Azure Information Protection
6. If you experience issues and you use Citrix, make sure to disable Citrix hooking as described here: [How to Disable Citrix API Hooks on a Per-application Basis](https://support.citrix.com/article/CTX107825) and exclude all Office apps
7. If you have Excel spreadsheets that contain macros, edit the macros as follows to ensure that they continue to work as expected after the Azure Information Protection client is installed:

    * At the beginning of the macro, add: `Application.EnableEvents = False`
	* At the end of the macro, add: `Application.EnableEvents = True`

8. If you are Windows Defender installed, run the following command in elevated (Run as Administrator) PowerShell session and see if issue resolves: `Set-ProcessMitigation -Name <app path> -Disable EAF, IAF` where instead of <app path> place the relevant exe paths to all Office apps (excel.exe, winword.exe, etc.)
9. If you are still experiencing the issue, collect Azure Information Protection client logs and attach the exported logs to this ticket

### Export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook
2. Select the **Protect** button -> **Help and feedback**
3. Select **Export Logs**
4. Save the logs to your choice of location, and attach them to this service request

## **Recommended Documents**

* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Review Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>
