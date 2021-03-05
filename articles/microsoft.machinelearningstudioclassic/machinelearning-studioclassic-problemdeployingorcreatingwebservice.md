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
	cloudEnvironments="public, usnat, ussec, fairfax"
	ownershipId="AzureML_AzureMachineLearning"
/>

# Problem deploying or creating web service

Resolve issues deploying or creating a web service using these steps.

## **Recommended Steps**

* To deploy experiment as a new web service, the user must have the **Contributor** role for the subscription that contains the workspace. Refer to [this article](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#contributor) to learn more about **Contributor** role. 

* If you're experiencing errors such as the following, authentication is likely the root cause:<br>
   "Error Message: Web Service deployment failed. This account does not have sufficient access to the Azure subscription that contains the Workspace. In order to deploy a Web Service to Azure, the same account must be invited to the Workspace and be given access to the Azure subscription that contains the Workspace."

   Authentication errors occur when users in multiple tenants and one or more tenants in multiple tenants require MFA (multi-factor authentication)
   There are two ways to fix this:

   - Use **Deploy Web Service [Classic]** instead of Web Service [New].  

   - Use an existing account, or create a new account, that **disables MFA** in your target tenant (the tenant to which your workspace belongs). Next, log in to your studio workspace using this account, and deploy web service.

## **Recommended Documents**

Microsoft Azure Machine Learning Studio (classic) is a collaborative, drag-and-drop tool you can use to build, test, and deploy predictive analytics solutions on your data. Customers currently using or evaluating Machine Learning Studio (classic) are encouraged to try [Azure Machine Learning designer](https://docs.microsoft.com/azure/machine-learning/concept-designer), which provides drag and drop ML modules plus scalability, version control, and enterprise security.
