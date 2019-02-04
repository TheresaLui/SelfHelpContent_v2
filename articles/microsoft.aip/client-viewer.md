<properties
	pageTitle="Azure Information Client - Viewer Issues"
	description="Azure Information Client - Viewer Issues"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	articleId="Viewer_Issues"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584328"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public"
/>

# Azure Information Client - Viewer Issues

## **Recommended Steps**

1. Verify you are logged in to Azure Information Protection with the correct permissions to open the file

2. If you have a firewall or similar intervening network devices that are configured to allow specific connections, see the information for **Azure Rights Management (RMS)** in the [Office 365 portal and shared](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2?ui=en-US&rs=en-US&ad=US#bkmk_portal-identity) section from the following Office article: [Office 365 URLs and IP address ranges](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2).

  Use the instructions in this Office article to keep up-to-date with changes to this information, by subscribing to an RSS feed.

  In addition to the information in the Office article, specific to Azure Information Protection:

  - Allow HTTPS traffic on TCP 443 to **api.informationprotection.azure.com**.

  - Allow HTTPS traffic on TCP 443 to **mobile.pipe.aria.microsoft.com**.

  - If you use a web proxy that requires authentication, you must configure it to use integrated Windows authentication with the user's Active Directory logon credentials.

  - Do not terminate the TLS client-to-service connections (for example, to do packet-level inspection) to the Azure Rights Management service. Doing so breaks the certificate pinning that RMS clients use with Microsoft-managed CAs to help secure their communication with the Azure Rights Management service.
[More information regarding Firewalls and network infrastructure requirements](https://docs.microsoft.com/azure/information-protection/get-started/requirements#firewalls-and-network-infrastructure)

## How to export Azure Information Protection Viewer logs

1. Open Azure Information Protection Viewer.
2. Click on Settings icon at the left bottom.
3. Click "Export Logs".
4. Save the logs in your desired location and attach it to this service request.

## **Recommended Documents**

[Download Azure Information Protection Viewer](https://www.microsoft.com/download/details.aspx?id=54536)<br>
[User Guide: View and use files that have been protected by Rights Management](https://docs.microsoft.com/azure/information-protection/rms-client/client-view-use-files)<br>
[Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
[Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)