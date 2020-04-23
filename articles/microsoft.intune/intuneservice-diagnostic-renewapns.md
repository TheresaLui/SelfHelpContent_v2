<properties
	pageTitle="APNs Diagnostic Renew"
	description="APNs Diagnostic Renew"
	infoBubbleText="Your Apple Push certificate has expired.  Please review the steps on the right for how to renew it."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	ms.author="jlynn"
	displayOrder=""
	articleId="intune_renew_apns"
	diagnosticScenario="IntuneCheckAPNSCert"
	selfHelpType="diagnostics"
	supportTopicIds="32599602,32599605,32599626,32599644,32599650,32599653,32599665,32599632"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="IntuneCxP_Intune"
/>

# We ran diagnostics on your Microsoft Intune subscription and found an issue

<!--issueDescription-->
The Apple MDM Push certificate has expired or is about to expire. If your Apple MDM Push certificate expires you'll be unable enroll iOS and MacOS devices and your existing devices will be unable to check-in to the Intune service.
<!--/issueDescription-->

The Apple MDM push certificate is valid for one year and must be renewed annually to maintain iOS and macOS device management. If your certificate expires, enrolled Apple devices cannot be contacted.

The certificate is associated with the Apple ID used to create it. Renew the MDM push certificate with the same Apple ID used to create it.

## **Recommended Steps**

1. In the [Azure portal](https://portal.azure.com/), choose **Device enrollment > Apple enrollment**, and then **choose the Apple MDM Push certificate** tile in the details area
2. Choose **Download your CSR** to download and save the request file locally. The file is used to request a trust relationship certificate from the Apple Push Certificates Portal.
3. Select **Create your MDM push Certificate** to go to the [Apple Push Certificates Portal](http://go.microsoft.com/fwlink/?LinkId=261984). Find the certificate you want to renew and **select Renew**.
4. On the Renew Push Certificate screen, provide notes to help you identify the certificate in the future, select **Choose File** to browse to the new request file you downloaded, and choose Upload.

	A Certificate can be identified by its UID. Examine the Subject ID in the certificate details to find the GUID portion of the UID. Or, on an enrolled iOS device, go to Settings > General > Device Management > Management Profile > More Details > Management Profile. The second line item, Topic, contains the unique GUID that you can match up to the certificate in the Apple Push Certificates portal.

5. On the Confirmation screen, **select Download** and save the .pem file locally
6. In the Azure portal, select the Apple MDM push certificate browse icon, select the .pem file downloaded from Apple, and **choose Upload**.  Your Apple MDM push certificate appears Active and has 365 days until expiration.
