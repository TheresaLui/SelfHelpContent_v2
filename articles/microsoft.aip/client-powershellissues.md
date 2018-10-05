<properties
	pageTitle="Azure Information Client - PowerShell issues"
	description="Azure Information Client - PowerShell issues"
	service="microsoft.aip"
	resource="aip"
	authors="nihendle"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584372"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public"
/>

# Azure Information Protection client - PowerShell issues

## Recommended troubleshooting steps

1. Verify your Windows PowerShell version is 4.0 or later by running **$PSVersionTable** in a PowerShell session. If you need to install a later version of Windows PowerShell, see [Upgrading existing Windows PowerShell](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell#upgrading-existing-windows-powershell).
2. Verify that the Azure Information Protection module is installed by running **Get-Module –ListAvailable** in a PowerShell session. If you do not see the **AzureInformationProtection** module, [install the Azure Information Protection client](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-install), which includes the Azure Information Protection module. 

If you still experience the issue, collect Azure Information Protection client logs and attach the exported logs to this ticket.

## How to export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook.
2. Select the **Protect** button -> **Help and feedback**.
3. Select **Export Logs**.
4. Save the logs to your choice of location, and attach them to this service request.

## **Recommended documents**

[Review Azure Information Protection documentation](https://aka.ms/aipdocs)<br>
[Review Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
[Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
[Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
[Using PowerShell with the Azure Information Protection client](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-powershell)