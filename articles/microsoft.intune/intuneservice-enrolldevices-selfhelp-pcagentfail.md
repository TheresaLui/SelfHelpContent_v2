<properties
	pageTitle="Installation of the PC client software fails with The software cannot be installed, 0x80cf4017"
	description="Installation of the PC client software fails with The software cannot be installed, 0x80cf4017"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="6"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="device_enrollment_selfhelp"
	productPesIds=""
	cloudEnvironments="public"
/>

# Installation of the PC client software fails with "The software cannot be installed, 0x80cf4017"

## **Recommended steps**

This error occurs when your account certificate has expired.  The account certificate that is used to enroll PC clients last for one year.  Re-download the PC Client software package in the Intune Admin Console and it will include an updated certificate.  For more information please review [this documentation](https://docs.microsoft.com/intune-classic/deploy-use/install-the-windows-pc-client-with-microsoft-intune).




