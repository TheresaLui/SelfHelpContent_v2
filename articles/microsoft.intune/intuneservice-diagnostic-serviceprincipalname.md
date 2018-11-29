<properties
	pageTitle="Service Principal Name disabled"
	description="Service Principal Name disabled"
	infoBubbleText="The Intune Service Principal has been disabled.  Please review the steps on the right for how to re-enable."
	service="microsoft.intune"
	resource="intune"
	authorAlias="jlynn"
	authors="mackie1604"
	displayOrder=""
	articleId="service_principal_disabled"
	diagnosticScenario="IntuneCheckAPNSCert"
	selfHelpType="diagnostics"
	supportTopicIds="32599602,32599605,32599626,32599644,32599650,32599653,32599665,32599632"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public"
/>

# We ran diagnostics on your Microsoft Intune subscription and found an issue

## Recommended steps

<!--issueDescription-->
Microsoft Intune has a dependency on specific Service Principals to function correctly. We allow the ability to disable these Intune SPN's in Azure Active Directory for customers that would like to do so.  We have detected that you are using Intune and that these SPN's are disabled which will prevent Intune from functioning correctly.  Please follow the steps below to enable the Intune SPN's.
<!--/issueDescription-->

Please re-enable sign on for **<!--$IntuneAppNames-->[IntuneAppNames]<!--/$IntuneAppNames -->**.

To remediate this situation we advise:

Step 1.  In the [Azure portal](https://portal.azure.com/), choose Azure Active Directory > Enterprise Applications, and then choose Application type of All Applications and hit apply.

Step 2.  Search for **<!--$IntuneAppNames-->[IntuneAppNames]<!--/$IntuneAppNames-->**.

Step 3.  Click the Application and then click Properties from the Management menu.

Step 4.  Set the enabled for sign on value to YES and hit save.

Step 5.  Navigate back to the Intune application in the Azure portal and confirm it's working as expected.
