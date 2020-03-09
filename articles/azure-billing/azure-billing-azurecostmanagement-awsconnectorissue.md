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
	cloudEnvironments="public, Fairfax, Blackforest, Mooncake"
	articleId="9e4e7b88-954c-4e1b-b883-1d9ba287acf51"
	ownershipId="ASMS_Billing"
/>

# Azure Cost Managment - AWS connector issue

## **Recommended Steps**

**Troubleshooting AWS integration**<br>

Use the following troubleshooting information to resolve common problems.

* **No permission to AWS Linked accounts**<br>

**Error code**: Unauthorized<br>

There are two ways to get permissions to access AWS linked accounts costs:

	* Get access to the management group that has the AWS Linked accounts
	* Have someone give you permission to the AWS linked account

By default, the AWS connector creator is the owner of all the objects that the connector created, including the AWS consolidated account and the AWS linked account. In order to be able to verify the connector settings, you will need at least a **contributor** role, as **reader** cannot verify connector settings.

* **Collection failed with AssumeRole**<br>
**Error code**: FailedToAssumeRole<br>
This error means that Cost Management is unable to call the AWS AssumeRole API. This problem can happen because of an issue with the role definition. Verify that the following conditions are true:
	* The external ID is the same as the one in the role definition and the connector definition
	* The role type is set to **Another AWS account Belonging to you or 3rd party**
	* The **Require MFA** choice is cleared
	* The trusted AWS account in the AWS Role is 432263259397

* **Collection failed with Access Denied - CUR report definitions**<br>
**Error code**: AccessDeniedReportDefinitions<br>
This error means that Cost Management is unable to see the Cost and Usage report definitions. This permission is used to validate that the CUR is defined as expected by Azure Cost Management. See [Create a Cost and Usage report in AWS](https://docs.microsoft.com/azure/cost-management-billing/costs/aws-integration-set-up-configure#create-a-cost-and-usage-report-in-aws).

* **Collection failed with Access Denied - List reports**<br>
**Error code**: AccessDeniedListReports<br>
This error means that Cost Management is unable to list the object in the S3 bucket where the CUR is located. AWS IAM policy requires a permission on the bucket and on the objects in the bucket. See [Create a role and policy in AWS](https://docs.microsoft.com/azure/cost-management-billing/costs/aws-integration-set-up-configure#create-a-role-and-policy-in-aws).

* **Collection failed with Access Denied - Download report**<br>
**Error code**: AccessDeniedDownloadReport
This error means that Cost Management is unable to access and download the CUR files stored in the Amazon S3 bucket. Make sure that the AWS JSON policy attached to the role resembles the example shown at the bottom of the [Create a role and policy in AWS](https://docs.microsoft.com/azure/cost-management-billing/costs/aws-integration-set-up-configure#create-a-role-and-policy-in-aws) section.

* **Collection failed since we did not find the Cost and Usage Report**<br>
**Error code**: FailedToFindReport<br>
This error means that Cost Management can't find the Cost and Usage report that was defined in the connector. Make sure it isn't deleted and that the AWS JSON policy attached to the role resembles the example shown at the bottom of the [Create a role and policy in AWS](https://docs.microsoft.com/azure/cost-management-billing/costs/aws-integration-set-up-configure#create-a-role-and-policy-in-aws) section.

* **Unable to create or verify connector due to Cost and Usage Report definitions mismatch**<br>
**Error code**: ReportIsNotValid<br>
This error relates to the definition of AWS Cost and Usage Report, we require specific settings for this report, see the requirements in [Create a Cost and Usage report in AWS](https://docs.microsoft.com/azure/cost-management-billing/costs/aws-integration-set-up-configure#create-a-cost-and-usage-report-in-aws).

## **Recommended Documents**

* [Troubleshooting AWS integration](https://docs.microsoft.com/azure/cost-management/aws-integration-manage#troubleshooting-aws-integration)<br>
* [Setup and configure AWS integration](https://docs.microsoft.com/azure/cost-management-billing/costs/aws-integration-set-up-configure)<br>
* [Manage AWS costs and usage in Azure](https://docs.microsoft.com/azure/cost-management/aws-integration-manage)<br>
* [AWS Integration Pricing](https://docs.microsoft.com/azure/cost-management/aws-integration-manage#aws-integration-pricing)<br>
