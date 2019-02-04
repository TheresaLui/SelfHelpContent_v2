<properties
	pageTitle="APNS setup correctly"
	description="APNS setup correctl"
	infoBubbleText="Your Apple Push Notification service is setup correctly"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	ms.author="jlynn"
	displayOrder=""
	articleId="apns_working_maven"
	diagnosticScenario="IntuneCheckAPNSCert"
	selfHelpType="diagnostics"
	supportTopicIds="32599602,32599605,32599626,32599644,32599650,32599653,32599665,32599632"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public"
/>

# We ran diagnostics on your Microsoft Intune subscription and found an issue

<div>
Review the resources listed below to resolve your issue now. 
<br/>
Some common error messages and resolution steps:
<br/><br/>
  <ol>
    <li>Device Cap Reached - The user has more devices enrolled than the device limit. Review these documents to <a href="https://docs.microsoft.com/en-us/intune/devices-wipe">remove a device</a> or <a href="https://docs.microsoft.com/en-us/intune/enrollment-restrictions-set#set-device-limit-restrictions">change the device limit</a>.</li>
    <li>This Service is not supported. No Enrollment Policy - Apple Push Notification Service (APNS) needs to be configured or renewed. Review <a href="https://docs.microsoft.com/en-us/intune/apple-mdm-push-certificate-get">this document</a> for instructions on how to do that.</li>
    <li>User License Type Invalid or User Name Not Recognized - The user needs to be assigned an Intune or EMS license. Review these documents to assign a license through: <a href="https://docs.microsoft.com/en-us/intune/licenses-assign">Office Admin Center</a> or <a href="https://docs.microsoft.com/en-us/azure/active-directory/license-users-groups">Azure portal<a/></li>
  </ol>
<br/>
	Additional resources to help resolve your issue:
  <ol>    
    <li>Use <a href="https://devicemanagement.microsoft.com/#blade/Microsoft_Intune_DeviceSettings/TroubleshootBlade">Intune Troubleshooting Portal</a> to diagnose and resolve common enrollment failures. Review <a href="https://docs.microsoft.com/en-us/intune/help-desk-operators">this document</a> for more details.</li>
    <li>Review these documents for a list of common errors that prevent enrollment and resolutions to each: <a href="https://support.microsoft.com/en-us/help/4039809/troubleshooting-ios-device-enrollment-in-intune">Troubleshooting guide</a> and <a href="https://docs.microsoft.com/en-us/intune-classic/troubleshoot/troubleshoot-device-enrollment-in-intune">Troubleshooting doc</a>.</li>
    <li><a href="https://docs.microsoft.com/en-us/intune/ios-enroll">Learn how to enroll iOS devices in Microsoft Intune</a>.</li>
  </ol>
</div>
