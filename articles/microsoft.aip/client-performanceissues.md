<properties
	pageTitle="Azure Information Client - Performance issues"
	description="Azure Information Client - Performance issues"
	service="microsoft.aip"
	resource="aip"
	authors="nihendle"
	ms.author="nihendle, orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584367"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="fe41ad8e-58bc-427f-8948-83e254775d08"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection client - performance issues

## **Recommended Steps**

1. Disable all enabled add-ins except **Microsoft Azure Information Protection** and verify if the issue persists
2. If the issue does not reproduce after disabling add-ins, enable them one by one to identify which one create the add-in clash
3. Temporarily disable all security products that are running, especially anti-virus services, and verify if the issue persists
4. Verify that your Office suite is updated to the latest version
5. Verify the [firewall and network requirements](https://docs.microsoft.com/azure/information-protection/get-started/requirements#firewalls-and-network-infrastructure) for Azure Information Protection
6. If you have Excel spreadsheets that contain macros, edit the macros as follows to ensure that they continue to work as expected after the Azure Information Protection client is installed:

    * At the beginning of the macro, add: `Application.EnableEvents = False`
	* At the end of the macro, add: `Application.EnableEvents = True`

7. Try to upgrade to the latest .NET Framework 4.8 which contain performance improvements: [Download .NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/net48)
8. If you are still experiencing the issue, collect Azure Information Protection client logs and attach the exported logs to this ticket

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
