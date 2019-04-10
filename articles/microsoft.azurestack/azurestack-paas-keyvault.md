<properties
    pageTitle="Azure Stack Key Vault"
    description="Azure Stack Key Vault article"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629222"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
	articleId="12ee57f8-1913-4da0-9d90-1deab56a0216"
/>

# Azure Stack Key Vault

An Azure Stack operator can sign in with an Azure Stack subscription, create a vault for the organization in which to store keys, and then be responsible for these operational tasks:

- Create or import a key or secret
- Revoke or delete a key or secret
- Authorize users or applications to access the key vault, so they can then manage or use its keys and secrets
- Configure key usage (for example, sign or encrypt)
- Provide developers with Uniform Resource Identifiers (URIs) to call from their applications
- Provide security administrators with key-usage logging information

## **Recommended Steps**

1. To create a Key Vault or manage keys and secrets in the portal, refer to the [manage Key Vault in Azure Stack by using the portal](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-kv-manage-portal) guide
2. To enable tenant subscriptions for Key Vault operations or to authorize an application to use a key or secret, refer to the [manage Key Vault in Azure Stack using PowerShell](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-kv-manage-powershell) guide
3. Compare your usage to a [sample application that uses keys and secrets stored in a key vault](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-kv-sample-app)

## **Recommended Documents**

* [Manage Key Vault in Azure Stack by using the portal](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-kv-manage-portal)
* [Manage Key Vault in Azure Stack using PowerShell](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-kv-manage-powershell)
* [Sample application that uses keys and secrets stored in a key vault](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-kv-sample-app)
