<properties
	pageTitle="APNs Diagnostic Setup"
	description="APNs Diagnostic Setup"
	infoBubbleText="The Apple Push certificate has not been setup.  Please review the steps on the right to set it up."
	service="microsoft.intune"
	resource="intune"
	ms.author="jlynn"
	authors="mackie1604"
	displayOrder=""
	articleId="intune_setup_apns"
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
An Apple MDM Push certificate has not been configured on your subscription. Without an Apple MDM Push certificate configured, you'll be unable to enroll iOS and MacOS devices. Intune enables mobile device management (MDM) of iPads, iPhones, and Mac computers and gives users access to company email and apps. An MDM Push certificate is required for Intune to manage iOS and Mac devices. After you add the certificate to Intune, your users can install the Company Portal app to enroll their devices.
<!--/issueDescription-->

## **Recommended Steps**

In the [Azure portal](https://portal.azure.com/), choose Device enrollment > Apple enrollment > Apple MDM Push certificate, and then follow these steps:

1. Grant Microsoft permission to send user and device information to Apple. Select **"I agree."** to give Microsoft permission to send data to Apple.
2. Download the Intune certificate signing request required to create an Apple MDM push certificate. Select **Download your CSR** to download and save the request file locally. The file is used to request a trust relationship certificate from the Apple Push Certificates Portal.
3. Create an Apple MDM push certificate. Select **Create your MDM push Certificate** to go to the [Apple Push Certificates Portal](http://go.microsoft.com/fwlink/?LinkId=261984). Sign in with your company Apple ID, and then click **Create a Certificate**. Select **Choose File** and browse to the certificate signing request file, and then choose **Upload**. On the Confirmation page, choose **Download** to the download the certificate (.pem) file, and save the file locally.

	**Note**: The certificate is associated with the Apple ID used to create it. As a best practice, use a company Apple ID for management tasks and make sure the mailbox is monitored by more than one person like a distribution list. Never use a personal Apple ID.

4. Enter the Apple ID used to create your Apple MDM push certificate. Record this ID as a reminder for when you need to renew this certificate.
5. Browse to your Apple MDM push certificate to upload. Go to the certificate (.pem) file, choose **Open**, and then choose **Upload**. With the push certificate, Intune can enroll and manage Apple devices.
