<properties
	articleId="af581b84-255e-4ffa-a45e-e0b3adc3aef8"
	articleTags="costanalysis,data, connectors"
	pageTitle="I’m unable to create a connector using my AWS credentials"
	description="How to setup connector"
	displayOrder="2"
	authors="shasulin"
	ms.author="shasulin"
	selfHelpType="resource"
	service="microsoft.costmanagement"
	resource="connectors"
	resourceTags=""
	productPesIds="15659"
	supportTopicIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	ownershipId="ASMS_Billing"
/>

# I want to view my Azure and AWS costs together

In order to view Azure and AWS costs together, we take the help of Management Group scopes in Azure and follow the steps: <br>

1. Create a Management Group or select an existing one.<br>
2. Assign existing and appropriate Azure subscriptions to the management group <br>
3. Assign the SAME Management Group to the Linked Account of the connector.<br>  
4. Go to Cost Analysis and select Accumulated costs<br> 
5. Select Group by Provider<br>  


## **Recommended Documents**

* [Troubleshooting AWS integration](https://docs.microsoft.com/azure/cost-management-billing/costs/aws-integration-set-up-configure)
* [Manage AWS costs and usage](https://docs.microsoft.com/azure/cost-management-billing/costs/aws-integration-manage)
* [AWS scopes](https://docs.microsoft.com/azure/cost-management-billing/costs/understand-work-scopes#aws-scopes)
