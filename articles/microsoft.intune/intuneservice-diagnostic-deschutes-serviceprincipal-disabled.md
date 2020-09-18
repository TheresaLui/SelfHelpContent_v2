<properties
	pageTitle="CloudPC Service Principal Name disabled"
	description="CloudPC Service Principal Name disabled"
	infoBubbleText="The CloudPC Service Principal has been disabled. Please review and complete the steps on the right to re-enable."
	service="microsoft.intune"
	resource="intune"
	ms.author="pphadke"
	authors=""
	displayOrder=""
	articleId="deschutes_service_principal_disabled"
	diagnosticScenario="DeschutesDiagnostics"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="IntuneCxP_Intune"
/>

# We ran diagnostics on your Microsoft CloudPC subscription and found an issue

<!--issueDescription-->
Microsoft CloudPC has a dependency on specific Service Principals (SPNs) to function correctly. We allow the ability to disable this CloudPC SPN in Azure Active Directory for customers that would like to do so. We have detected that you are using CloudPC and that its SPN is disabled, which will prevent CloudPC from functioning correctly. Please re-enable sign on for **<!--$CloudPCAppName-->[CloudPCAppName]<!--/$CloudPCAppName-->**.
<!--/issueDescription-->

## **Recommended Steps**

1. In the [Azure portal](https://portal.azure.com/), choose Azure Active Directory > Enterprise Applications, then choose the Application type of "All Applications" and click apply
2. Search for **<!--$CloudPCAppName-->[CloudPCAppName]<!--/$CloudPCAppName-->**
3. Click the application, then click "Properties" from the Management menu
4. Set the "enabled for sign on" value to YES
5. Click Save
6. Return to the Intune application in the Azure portal and confirm it's working as expected
