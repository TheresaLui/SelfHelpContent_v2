<properties
	pageTitle="Service Principal Name disabled"
	description="Service Principal Name disabled"
	infoBubbleText="The Intune Service Principal has been disabled. Please review and complete the steps on the right to re-enable."
	service="microsoft.intune"
	resource="intune"
	ms.author="jlynn"
	authors="mackie1604"
	displayOrder=""
	articleId="service_principal_disabled"
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
Microsoft Intune has a dependency on specific Service Principals (SPNs) to function correctly. We allow the ability to disable these Intune SPNs in Azure Active Directory for customers that would like to do so. We have detected that you are using Intune and that these SPNs are disabled, which will prevent Intune from functioning correctly. Please re-enable sign on for **<!--$IntuneAppNames-->[IntuneAppNames]<!--/$IntuneAppNames-->**.
<!--/issueDescription-->

## **Recommended Steps**

1. In the [Azure portal](https://portal.azure.com/), choose Azure Active Directory > Enterprise Applications, then choose the Application type of "All Applications" and click apply
2. Search for **<!--$IntuneAppNames-->[IntuneAppNames]<!--/$IntuneAppNames-->**
3. Click the application, then click "Properties" from the Management menu
4. Set the "enabled for sign on" value to YES
5. Click Save
6. Return to the Intune application in the Azure portal and confirm it's working as expected
