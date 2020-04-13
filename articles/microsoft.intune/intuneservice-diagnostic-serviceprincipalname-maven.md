<properties
	pageTitle="Service Principal Name disabled"
	description="Service Principal Name disabled"
	infoBubbleText="The Intune Service Principal has been disabled. Please review and complete the steps on the right to re-enable."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	ms.author="jlynn"
	displayOrder=""
	articleId="service_principal_disabled_maven"
	diagnosticScenario="IntuneCheckAPNSCert"
	selfHelpType="diagnostics"
	supportTopicIds="32599602,32599605,32599626,32599644,32599650,32599653,32599665,32599632"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="IntuneCxP_Intune"
/>

# We ran diagnostics on your Microsoft Intune subscription and found an issue

<div>
  Microsoft Intune has a dependency on specific Service Principals to function correctly. We allow the ability to disable these Intune SPN's in Azure Active Directory for customers that would like to do so. We have detected that you are using Intune and that these SPN's are disabled which will prevent Intune from functioning correctly. Please follow the steps below to enable the Intune SPN's.
  <br/><br/>
  <ol>
    <li>In the <a href="https://portal.azure.com">Azure portal</a>, choose Azure Active Directory | Enterprise Applications, and then choose Application type of All Applications and hit apply.</li>
    <li>Search for Microsoft Intune.</li>
    <li>Click the Applications returned and then click Properties from the Management menu.</li>
    <li>Ensure each one is has the "enabled for sign on" value to YES and hit save.</li>
    <li>Navigate back to the Intune application in the Azure portal and confirm it's working as expected.</li>
  </ol>
</div>
