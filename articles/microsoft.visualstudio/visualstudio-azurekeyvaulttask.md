<properties
	pageTitle="Azure KeyVault"
	description="Troubleshooting issues related to key vault access, firewall settings, secret or any guidance with the usage of the task"
	infoBubbleText="Azure Pipelines issues related to Azure KeyVault task"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AzureKeyVaultTask"
	supportTopicIds="32742298"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues while making use of Azure Key Vault task

## **Recommended Steps**

Are you facing one of these common problems?

* Key vault task doesn't download keys

    [Refer to this document](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-key-vault?view=azure-devops#yaml-snippet). You can also make use of a Powershell task and add your script in it to achieve this.

* Access KeyVault with firewall on through DevOps
	
    [Refer this document](https://docs.microsoft.com/azure/key-vault/general/access-behind-firewall)

* Problems Accessing Key Vault Data from AzureDevOps Build Pipeline - ARM service connection authentication errors

    Ensure that the **application ID** for the service connection matches the **application ID of the SPN in AAD** for which the permissions are granted. If it different, create a new **App Registration** with the proper permissions and adding the SPN as a new ARM service connection in Azure DevOps.

* I'm trying to use **Azure Key Vault** in an ARM template

    [Tutorial to integrate Azure Key Vault in your ARM template deployment](https://docs.microsoft.com/azure/azure-resource-manager/templates/template-tutorial-use-key-vault)

* Accessing Key Vault Secrets in Bash task

    Make use of both **replace tokens** and **bash task** in order to get the expected results.

* I'm not able to connect to Azure Key Vault from Azure DevOps

    Ensure the Azure service connection has at least Get and List management permissions on the vault for secrets.

## **Recommended Documents**

* [Azure Key Vault Task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-key-vault?view=azure-devops#yaml-snippet)
* [Access Azure Key Vault behind a firewall](https://docs.microsoft.com/azure/key-vault/general/access-behind-firewall)
* [Tutorial: Integrate Azure Key Vault in your ARM template deployment](https://docs.microsoft.com/azure/azure-resource-manager/templates/template-tutorial-use-key-vault)
* [Use secrets from Azure Key Vault in Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/release/azure-key-vault?view=azure-devops)
* [Link secrets from an Azure key vault](https://docs.microsoft.com/azure/devops/pipelines/library/variable-groups?view=azure-devops&tabs=yaml#link-secrets-from-an-azure-key-vault)
