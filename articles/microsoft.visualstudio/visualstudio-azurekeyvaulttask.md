<properties
  pagetitle="Azure pipelines issues while making use of Azure Key Vault task"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="v-abiss,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742298"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azurekeyvaulttask"
  ownershipid="Azure_DevOps_Services" />
# Azure pipelines issues while making use of Azure Key Vault task

## **Recommended Steps**

* Key Vault task doesn't download keys

    See [Azure Key Vault YAML snippet](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-key-vault?view=azure-devops#yaml-snippet). You can also add your script to a PowerShell task to resolve this issue.

* Access Key Vault with firewall on through Azure DevOps
	
    See [Access behind the firewall](https://docs.microsoft.com/azure/key-vault/general/access-behind-firewall)

* Problems accessing Key Vault data from the Azure DevOps Build Pipeline (ARM service connection authentication errors)

    Ensure that the **application ID** for the service connection matches the **application ID of the SPN in AAD** for which the permissions are granted. If it's different, create a new **App Registration** with the proper permissions, and adding the SPN as a new ARM service connection in Azure DevOps.

* I'm trying to use **Azure Key Vault** in an ARM template

    [Tutorial: Integrate Azure Key Vault in your ARM template deployment](https://docs.microsoft.com/azure/azure-resource-manager/templates/template-tutorial-use-key-vault)

* Accessing Key Vault Secrets in Bash task

    Make use of both the **replace tokens** and the **bash task** to get the expected results.

* I'm not able to connect to Azure Key Vault from Azure DevOps

    Ensure that the Azure service connection has at least the Get and List management permissions on the vault for secrets.

## **Recommended Documents**

* [Azure Key Vault Task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-key-vault?view=azure-devops#yaml-snippet)
* [Access Azure Key Vault behind a firewall](https://docs.microsoft.com/azure/key-vault/general/access-behind-firewall)
* [Tutorial: Integrate Azure Key Vault in your ARM template deployment](https://docs.microsoft.com/azure/azure-resource-manager/templates/template-tutorial-use-key-vault)
* [Use secrets from Azure Key Vault in Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/release/azure-key-vault?view=azure-devops)
* [Link secrets from an Azure key vault](https://docs.microsoft.com/azure/devops/pipelines/library/variable-groups?view=azure-devops&tabs=yaml#link-secrets-from-an-azure-key-vault)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
