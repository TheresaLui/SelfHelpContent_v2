<properties
	pageTitle="Enrolling a Windows 10 PC via MDM fails with error code 0x801c0003"
	description="Enrolling a Windows 10 PC via MDM fails with error code 0x801c0003"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="5"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags="device_enrollment_selfhelp"
	productPesIds=""
	cloudEnvironments="public"
/>

# Enrolling a Windows 10 PC via MDM fails with error code 0x801c0003"

## **Recommended steps**

The error can occur in the following scenarios.  **1.** Device cap reached.  Unenroll devices for the user and try again.  **2.** If "Allow Devices to join Azure AD" is set to none.  **3.** The device is already enrolled by another user. Confirm the if device is enrolled.  **4.** The device is Windows 10 Home.  Only Windows 10 Pro, Education and Enterprise skus are allowed to join Azure Active Directory.  



