<properties
	pageTitle="Azure Information Client - Manual protection"
	description="Azure Information Client - Manual protection"
	service="microsoft.aip"
	resource="aip"
	authors="nihendle"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584355"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public"
/>

# Azure Information Client - Manual protection

## Recommended troubleshoot steps

1. Verify you are logged in to Azure Information Protection with the same user you logged into Office.

2. If you have a firewall or similar intervening network devices that are configured to allow specific connections, see the information for **Azure Rights Management (RMS)** in the [Office 365 portal and shared](https://support.office.com/en-us/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2?ui=en-US&rs=en-US&ad=US#bkmk_portal-identity) section from the following Office article: [Office 365 URLs and IP address ranges](https://support.office.com/en-US/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2).

  Use the instructions in this Office article to keep up-to-date with changes to this information, by subscribing to an RSS feed.

  In addition to the information in the Office article, specific to Azure Information Protection:

  - Allow HTTPS traffic on TCP 443 to **api.informationprotection.azure.com**.

  - Allow HTTPS traffic on TCP 443 to **mobile.pipe.aria.microsoft.com**.

  - If you use a web proxy that requires authentication, you must configure it to use integrated Windows authentication with the user's Active Directory logon credentials.

  - Do not terminate the TLS client-to-service connections (for example, to do packet-level inspection) to the Azure Rights Management service. Doing so breaks the certificate pinning that RMS clients use with Microsoft-managed CAs to help secure their communication with the Azure Rights Management service.
[More information regarding Firewalls and network infrstructure requirments](https://docs.microsoft.com/en-us/azure/information-protection/get-started/requirements#firewalls-and-network-infrastructure)

2. Verify if you have Azure AIP onboarding policy enabled, [More information can be found here.](https://docs.microsoft.com/en-us/azure/information-protection/deploy-use/activate-service#configuring-onboarding-controls-for-a-phased-deployment)

If you still experience the issue, please collect AIP logs with selecting "Export logs" from the "Protect -> Help and feedback" The **Export Logs** automatically collects and attaches log files for the Azure Information Protection client if you have been asked to send these to Microsoft Support. This option can also be used by end users to send these log files to your help desk. **Please attach the exported logs to this ticket**

In case you have **issues with installing** the client itself, please go to folder %temp% and provide the AIP installation log files that start with "Microsoft_Azure_Information_Protection_XXXXXXXXXX.log".

## How to export Azure Information Protection logs

1. Open Office document or new mail in Outlook.
2. Click on Protect button -> Help and feedback.
3. Click "Export Logs".
4. Save the logs in your desired location and attach it to this service request.

## **Recommended documents**

[Review Azure Information Protection documentation](https://aka.ms/aipdocs)<br>
[Review Azure Information Protection subscriptions and features](https://azure.microsoft.com/en-us/pricing/details/information-protection)<br>
[Requirements for Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/get-started/requirements)<br>
[Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>