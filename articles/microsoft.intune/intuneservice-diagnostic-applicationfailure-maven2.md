<properties
	pageTitle="Intune Application Diagnostic failure"
	description="Intune Application Diagnostic failure"
	infoBubbleText="Intune Application Diagnostic failure"
	service="microsoft.intune"
	resource="intune"
	ms.author="jlynn"
	authors="mackie1604"
	displayOrder=""
	articleId="intune_user_app_install_diagnostic"
	diagnosticScenario="Intuneapplicationdiagnosticfailure"
	selfHelpType="diagnostics"
	supportTopicIds="32599602,32599605,32599626,32599644,32599650,32599653,32599665,32599632"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="IntuneCxP_Intune"
/>

# We ran diagnostics on your Microsoft Intune subscription and found an issue.

<div>
Microsoft Intune has detected an application installation failure for <b><!--$UPN-->[UPN]<!--/$UPN--></b>. Please review the steps below to resolve:
<br/><br/>
User <!--$UPN-->[UPN]<!--/$UPN--> has experienced <!--$CountOfFailures-->[CountOfFailures]<!--/$CountOfFailures--> application installation failures across <!--$CountOfDevices-->[CountOfDevices]<!--/$CountOfDevices--> devices in the past 30 days.
<br/><br/>
The most recent app install error occurred on <!--$FailureDate-->[FailureDate]<!--/$FailureDate--> on the device whose ID is <!--$DeviceId-->[DeviceId]<!--/$DeviceId-->
<br/><br/>
<b>Application installation failed with the error:</b> <!--$ErrorCode-->[ErrorCode]<!--/$ErrorCode-->
<br/><br/>
<b>Failure description:</b> <!--$FailureDetails-->[FailureDetails]<!--/$FailureDetails-->
<br/><br/>
<b>How to resolve this failure:</b> <!--$FailureRemediation-->[FailureRemediation]<!--/$FailureRemediation-->
<br/><br/>
To troubleshoot the most recent failure, go to the <a href="<!--$ManagedAppViewLink-->[ManagedAppViewLink]<!--/$ManagedAppViewLink-->" target="_blank">Managed App View</a> for the device.
<br/><br/>
To troubleshoot all of this user’s application installation failures go to the <a href="https://go.microsoft.com/fwlink/?linkid=2113020" target="_blank">Intune Troubleshooting blade</a>.
</div>
