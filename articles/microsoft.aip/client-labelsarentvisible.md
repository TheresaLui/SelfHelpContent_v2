<properties
	pageTitle="Azure Information Client - Labels aren't visible"
	description="Azure Information Client - Labels aren't visible"
	service="microsoft.aip"
	resource="aip"
	authors="nihendle"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584353"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public"
/>

# Azure Information Protection client - labels aren't visible

## Recommended troubleshooting steps

If your issue is with a label that applies protection, verify the following:

1. You are using an [edition of Office that supports protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements#applications), such as Office 365 ProPlus.

2. You are signed in with the correct Azure AD user for your tenant.

   To check your signed-in account, select the **Protect** button -> **Help and Feedback**, and view user account that's displayed.

3. If the label is visible in some Office apps but not all Office apps, check whether the label is configured for the **Set user-defined permissions** option: - If this option is enabled and **In Outlook apply Do Not Forward** is selected, the label displays in Outlook only.
- If this option is enabled and **In Word, Excel, PowerPoint and File Explorer prompt user for custom permissions** is selected, the label displays in Word, Excel, PowerPoint and File Explorer, but not Outlook.


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
[Download Azure Information Protection client](http://aka.ms/aipclient)<br>