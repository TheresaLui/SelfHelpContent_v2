<properties
    pageTitle="TSG Summary - AD Auth for Azure Files Issues"
    description="TSG Summary - AD Auth for Azure Files Issues"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="TSG_Content"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="0ed7ceda-ed48-418e-a534-0d11278306ee"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# AD Auth for Azure Files TSG

This troubleshooter will guide you to find  root cause and resolution for AD Authentication for Azure Files issues. If your customer has advisory questions, there is a good chance that we have covered those in our existing documentation. 

Please review them first before you start. If these don't help, please reach out to our SMEs using [this teams channel](https://teams.microsoft.com/l/channel/19%3ab08416c6a6054c029ce025987dc70850%40thread.skype/AD%2520DS%2520Auth%2520for%2520Azure%2520Files?groupId=082ae864-dfc1-4ae5-b096-6e1e878b339e&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47). 

1. Overview: https://docs.microsoft.com/azure/storage/files/storage-files-active-directory-overview
2. Enablement: https://docs.microsoft.com/azure/storage/files/storage-files-identity-auth-active-directory-enable
3. FAQ: https://docs.microsoft.com/azure/storage/files/storage-files-faq#ad-ds--azure-ad-ds-authentication
4. Troubleshooting: https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems

In order to start, please verify using ASC if the customer has AD Auth Enabled on the Storage Account by following below steps. 

1. Go to ASC Resource Explorer
2. Select customer's storage account
3. Under configuration, verify if "Identity-based Directory Service for Azure File Authentication" property is set to AD.(Note: Value "AAD" means customer has Azure AD Auth setup on their account and this troubleshooter does not apply to that topic.)
