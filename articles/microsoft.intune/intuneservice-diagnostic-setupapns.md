<properties
	pageTitle="APNs Diagnostic Setup"
	description="APNs Diagnostic Setup"
	infoBubbleText="Found issue with APNs. See details on the right."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder=""
	articleId="intune_setup_apns"
	selfHelpType="diagnostic"
	supportTopicIds="32599602,32599605,32599626,32599644,32599650,32599653,32599665"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public"
/>

# We ran diagnostics on your Microsoft Intune subscription and found an issue

<!--issueDescription-->
Currently an Apple Push Notification service (APNs) certificate has not been configured on your subscription.  Without an APNs configured you'll be unable enroll iOS and MacOS devices.
<!--/issueDescription-->

Intune enables mobile device management (MDM) of iPads, iPhones, and Mac computers and gives users access to company email and apps. An MDM Push certificate is required for Intune to manage iOS and Mac devices. After you add the certificate to Intune, your users can install the Company Portal app to enroll their devices. You can also set up corporate-owned iOS device management with Apple's Device Enrollment Program or enroll devices using Apple Configurator, for example.

In the [Azure portal](https://portal.azure.com/), choose Device enrollment > Apple Enrollment > Apple MDM Push Certificate, and then follow these steps:

**Step 1.** Grant Microsoft permission to send user and device information to Apple.  Select "I agree." to give Microsoft permission to send data to Apple.

**Step 2.** Download the Intune certificate signing request required to create an Apple MDM push certificate.  Select Download your CSR to download and save the request file locally. The file is used to request a trust relationship certificate from the Apple Push Certificates Portal.

**Step 3.** Create an Apple MDM push certificate.  Select Create your MDM push Certificate to go to the Apple Push Certificates Portal. Sign in with your company Apple ID, and then click Create a Certificate. Select Choose File and browse to the certificate signing request file, and then choose Upload. On the Confirmation page, choose Download to the download the certificate (.pem) file, and save the file locally.

**Note**

The certificate is associated with the Apple ID used to create it. As a best practice, use a company Apple ID for management tasks and make sure the mailbox is monitored by more than one person like a distribution list. Never use a personal Apple ID.

**Step 4.** Enter the Apple ID used to create your Apple MDM push certificate.  Record this ID as a reminder for when you need to renew this certificate.

**Step 5.** Browse to your Apple MDM push certificate to upload.  Go to the certificate (.pem) file, choose Open, and then choose Upload. With the push certificate, Intune can enroll and manage Apple devices.
