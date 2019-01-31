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
2. If you have a firewall or similar intervening network devices that are configured to allow specific connections, review the [**Azure Rights Management (RMS)**](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2?ui=en-US&rs=en-US&ad=US#bkmk_portal-identity) policy
3. Subscribe to an RSS feed for the above article to keep up-to-date with changes
4. In addition to the information in the Office article, specific to Azure Information Protection:

	* Allow HTTPS traffic on TCP 443 to **api.informationprotection.azure.com**
	* Allow HTTPS traffic on TCP 443 to **mobile.pipe.aria.microsoft.com**
	* If you use a web proxy that requires authentication, you must configure it to use integrated Windows authentication with the user's Active Directory logon credentials
	* Do not terminate the [TLS client-to-service connections to the Azure Rights Management service](https://docs.microsoft.com/azure/information-protection/get-started/requirements#firewalls-and-network-infrastructure), as doing so will break the certificate pinning that RMS clients use with Microsoft-managed CAs to help secure their communication with the Azure Rights Management service

### Export Azure Information Protection Viewer logs

1. Open Azure Information Protection Viewer
2. Click on Settings icon at the left bottom
3. Click "Export Logs"
4. Save the logs in your desired location and attach it to this service request

## **Recommended Documents**

* [Download Azure Information Protection Viewer](https://www.microsoft.com/download/details.aspx?id=54536)<br>
* [User Guide: View and use files that have been protected by Rights Management](https://docs.microsoft.com/azure/information-protection/rms-client/client-view-use-files)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
