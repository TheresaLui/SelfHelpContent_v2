<properties
	pageTitle="Problem deploying or creating web service"
	description="Problem deploying or creating web service"
	infoBubbleText="Problem deploying or creating web service"
	service="microsoft.machinelearningstudioclassic"
	resource="studioclassic"
	authors="likebupt"
	ms.author="keli19"
	articleId="machinelearning-studioclassic-problemdeployingorcreatingwebservice"
	selfHelpType="generic"
	supportTopicIds="32321850"
	productPesIds="15570"
	cloudEnvironments="public, usnat, ussec"
	ownershipId="AzureML_StudioClassicServices"
/>

# Problem deploying or creating web service

## **Recommended Steps**

1. For errors like "Error Message: Web Service deployment failed. This account does not have sufficient access to the Azure subscription that contains the Workspace. In order to deploy a Web Service to Azure, the same account must be invited to the Workspace and be given access to the Azure subscription that contains the Workspace.", the root cause is authentication, **Deploy Web Service [Classic]** is recommended.
1. When user’s in multiple tenants and one or more tenants required MFA (multi-factor authentication), the error above might occur. There are two ways user could have a try:

    - Create a new account in your target tenant (where your workspace belongs to). 
    - Or one existing account which only exists in the target tenant, invite this account to your studio workspace and assign proper role to it in your subscription.

Then try to login to your studio workspace use this account and deploy webservice to see if it works.


## **Recommended Documents**
Microsoft Azure Machine Learning Studio (classic) is a collaborative, drag-and-drop tool you can use to build, test, and deploy predictive analytics solutions on your data. Customers currently using or evaluating Machine Learning Studio (classic) are encouraged to try [Azure Machine Learning designer](https://docs.microsoft.com/azure/machine-learning/concept-designer), which provides drag and drop ML modules plus scalability, version control, and enterprise security.