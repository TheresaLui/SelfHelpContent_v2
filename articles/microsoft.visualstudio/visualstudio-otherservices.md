<properties
  pagetitle="Using Azure services and configurations with Azure Pipeline&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="v-abiss,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742324"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azureotherservices"
  ownershipid="Azure_DevOps_Services" />
# Using Azure services and configurations with Azure Pipeline

This article answers common questions about Azure Pipelines.

* **I want to add the Azure Policy Compliance task to the build/release pipeline.**

    The **Policy Compliance Configuration** can be configured only by using the approval gates within a release pipeline. It can't be used as a task in the build or release pipeline. See [Azure policy](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-policy?view=azure-devops).

* **Terraform crashes with the error: "eval: terraform.EvalApplyPost, err: rpc error: code = Unavailable desc = transport is closing"**

    Ensure you are using the Terraform task provided by Microsoft. You can find this in the [Marketplace](https://marketplace.visualstudio.com/items?itemName=ms-devlabs.custom-terraform-tasks).

* **I want to create a trigger that runs a pipeline on a schedule for each month of deployment to Azure Data Factory**

    See [How to create a schedule trigger](https://docs.microsoft.com/azure/data-factory/how-to-create-schedule-trigger)

* **My Azure DevOps release pipeline for ADF can't access the storage account; therefore, I'm unable to deploy an ARM template to ADF from Azure DevOps**

    In this case, perform the following steps:
    * Open the firewall rules and restrict access by using short-lived [SAS tokens](https://docs.microsoft.com/azure/storage/common/storage-sas-overview)
    * Move the templates to an Azure DevOps or Github repository. You can probably keep your linked templates in the same ADF git repository.

## **Recommended Documents**

* [Configure an Azure VM cluster using Terraform](https://docs.microsoft.com/azure/developer/terraform/create-vm-cluster-module)
* [Create a Linux VM with infrastructure in Azure using Terraform](https://docs.microsoft.com/azure/developer/terraform/create-linux-virtual-machine-with-infrastructure)
* [Continuous integration and delivery in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment)
* [Continuous integration and delivery on Azure Databricks using Azure DevOps](https://docs.microsoft.com/azure/databricks/dev-tools/ci-cd/ci-cd-azure-devops)
* [Create a trigger that runs a pipeline on a schedule](https://docs.microsoft.com/azure/data-factory/how-to-create-schedule-trigger)
* [Linked services in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-linked-services)
* [Pipelines and activities in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-pipelines-activities)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
