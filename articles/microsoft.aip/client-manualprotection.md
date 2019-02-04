<properties
	pageTitle="Azure Information Client - Manual protection"
	description="Azure Information Client - Manual protection"
	service="microsoft.aip"
	resource="aip"
	authors="nihendle"
	ms.author="nihendle, orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584355"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public"
	articleId="4cbe85cf-4914-4ec8-a86a-97e676b357bb"
/>

# Azure Information Client - Manual protection

## **Recommended Steps**

1. Verify you are logged in to Azure Information Protection with the same user you logged into Office
2. If you have a firewall or similar intervening network devices that are configured to allow specific connections, review the information for **Azure Rights Management (RMS)** in the [Office 365 portal and shared](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2?ui=en-US&rs=en-US&ad=US#bkmk_portal-identity) documentation. Use the instructions in this Office article to keep up-to-date with changes to this information, by subscribing to an RSS feed.
3. In addition to the information in the Office article, specific to Azure Information Protection:

  - Allow HTTPS traffic on TCP 443 to **api.informationprotection.azure.com**
  - Allow HTTPS traffic on TCP 443 to **mobile.pipe.aria.microsoft.com**
  - If you use a web proxy that requires authentication, you must configure it to use integrated Windows authentication with the user's Active Directory logon credentials
  - Do not terminate the [TLS client-to-service connections](https://docs.microsoft.com/azure/information-protection/get-started/requirements#firewalls-and-network-infrastructure) (for example, to do packet-level inspection) to the Azure Rights Management service. Doing so breaks the certificate pinning that RMS clients use with Microsoft-managed CAs to help secure their communication with the Azure Rights Management service.

2. Verify if you have [Azure AIP onboarding policy](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service#configuring-onboarding-controls-for-a-phased-deployment) enabled
3. If you are still experiencing the issue, please collect AIP logs with selecting "Export logs" from the "Protect -> Help and feedback". The **Export Logs** automatically collects and attaches log files for the Azure Information Protection client if you have been asked to send these to Microsoft Support. This option can also be used by end users to send these log files to your help desk. **Please attach the exported logs to this ticket**.
4. If you have **issues with installing** the client itself, please go to folder %temp% and provide the AIP installation log files that start with "Microsoft_Azure_Information_Protection_XXXXXXXXXX.log"

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
