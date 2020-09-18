<properties
	pageTitle="Cloud PC Service Principal Name disabled"
	description="Cloud PC Service Principal Name disabled"
	infoBubbleText="The Cloud PC Service Principal has been disabled. Please review and complete the steps on the right to re-enable."
	service="microsoft.intune"
	resource="intune"
	ms.author="pphadke"
	authors=""
	displayOrder=""
	articleId="cloudpc_service_principal_disabled"
	diagnosticScenario="CloudPCDiagnostics"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="IntuneCxP_Intune"
/>

# We ran diagnostics on your Microsoft Cloud PC subscription and found an issue

<!--issueDescription-->
Microsoft Cloud PC has a dependency on a specific Service Principal Name (SPN) to function correctly. The ability to disable this Cloud PC SPN is available in Azure Active Directory for customers that wish to do so. We have detected that you are using Cloud PC and that its SPN is disabled, which will prevent Cloud PC from functioning correctly. Please re-enable sign on for **<!--$CloudPCAppName-->[CloudPCAppName]<!--/$CloudPCAppName-->**.
<!--/issueDescription-->

## **Recommended Steps**

1. In the [Azure portal](https://portal.azure.com/), choose Azure Active Directory > Enterprise Applications, then choose the Application type "All Applications" and click Apply
2. Search for **<!--$CloudPCAppName-->[CloudPCAppName]<!--/$CloudPCAppName-->**
3. Click the application, then click "Properties" from the Management menu
4. Set the "Enabled for users to sign-in" value to Yes
5. Click Save
6. Return to the Microsoft Cloud PC application in the Azure portal and confirm it's working as expected
