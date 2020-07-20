<properties
	pageTitle="Azure Cost Management - AWS connector issue"
	description="Azure Cost Management - AWS connector issue"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32615306"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public, Fairfax, Blackforest, Mooncake, usnat, ussec"
	articleId="9e4e7b88-954c-4e1b-b883-1d9ba287acf51"
	ownershipId="ASMS_Billing"
/>

# Azure Cost Management - AWS connector issue

## **Recommended Steps**

**Troubleshooting AWS integration**<br>

* **I’m unable to create a connector using my AWS credentials**<br>
This may happen due to the following reasons:

  1. Invalid AWS credentials. Please check your AWS credentials and whether they are active.
  2. Only 1 connector can be created for a consolidated account. Hence, if someone has already created a connector for the same consolidated account, we suggest you reach out to them to grant you access to the connector.
  
 * **I want to view my Azure and AWS costs together**<br>
 In order to view Azure and AWS costs together, we take the help of Management Group scopes in Azure and follow the steps:
 
   1. Create a Management Group or select an existing one<br>
   2. Assign existing and appropriate Azure subscriptions to the management group<br>
   3. Assign the Same Management Group to the **Linked Account** of the connector<br>
   4. Go to **Cost Analysis** and select **Accumulated costs**<br>
   5. Select **Group by Provider**<br>

* **I want to change the Management Group of my Linked Account**<br>

   1. Click on the Connector which has the appropriate Linked Account<br>
   2. Click on Consolidated Account<br>
   3. Click on **Change Management Group**<br>
   4. Select the **Management Group and Linked Account**
   
## **Recommended Documents**

* [Troubleshooting AWS integration](https://docs.microsoft.com/azure/cost-management/aws-integration-manage#troubleshooting-aws-integration)<br>
* [Setup and configure AWS integration](https://docs.microsoft.com/azure/cost-management-billing/costs/aws-integration-set-up-configure)<br>
* [Manage AWS costs and usage in Azure](https://docs.microsoft.com/azure/cost-management/aws-integration-manage)<br>
* [AWS Integration Pricing](https://docs.microsoft.com/azure/cost-management/aws-integration-manage#aws-integration-pricing)<br>
