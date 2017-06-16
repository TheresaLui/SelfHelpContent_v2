<properties
	pageTitle="Set up iOS and Mac device management"
	description="Set up iOS and Mac device management"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32530435"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public"
/>

# Intune Enrollment iOS and Mac

## **Recommended steps**

The following is a list of errors that end users might see while enrolling iOS devices in Intune.

**Error Message:  Device Cap Reached**

* The user must remove one of his or her currently enrolled mobile devices from the Company Portal before enrolling another.

**Error Message:  No Enrollment Policy, APNSCertificateNotValid or AccountNotOnboarded**

* The Apple Push Notification Service (APNs) provides a channel to reach out to enrolled iOS devices. If the steps to get an APNs certificate were not performed, or if the APNs certificate has expired, then enrollment attempts will fail, and this message will appear.

**Error Message:  DeviceTypeNotSupported**

* Ensure that your user's device is running iOS version 8.0 or later.

**Error Message:  MdmAuthorityNotDefined**

* The mobile device management authority has not been designated in Intune.

## **Recommended documents**

[Troubleshoot device enrollment in Intune](https://docs.microsoft.com/intune/troubleshoot/troubleshoot-device-enrollment-in-intune)<br>
[Set up iOS and Mac device management](https://docs.microsoft.com/intune/deploy-use/set-up-ios-and-mac-management-with-microsoft-intune)<br>
[Enroll corporate-owned Device Enrollment Program iOS devices](https://docs.microsoft.com/intune/deploy-use/ios-device-enrollment-program-in-microsoft-intune#steps-to-enroll-ios-devices-by-using-apple-dep-management)<br>
[Wi-Fi connections in Microsoft Intune](https://docs.microsoft.com/intune/deploy-use/wi-fi-connections-in-microsoft-intune)<br>
[Azure AD federation compatibility list](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-compatibility)<br>
[Assign Intune licenses to your user accounts](https://docs.microsoft.com/intune/get-started/start-with-a-paid-subscription-to-microsoft-intune-step-4)<br>
[View licensed and unlicensed users with Office 365 PowerShell](https://technet.microsoft.com/library/dn771772.aspx)<br>
[Enroll your macOS device in Intune](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-macos)<br>



