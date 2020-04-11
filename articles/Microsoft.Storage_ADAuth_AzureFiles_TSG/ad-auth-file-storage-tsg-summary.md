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
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="0ed7ceda-ed48-418e-a534-0d11278306ee"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# AD Auth for Azure Files TSG

This troubleshooter will guide you to find the root cause and resolution for AD Authentication for Azure Files issues. In order to start, please verify using ASC if the customer has AD Auth Enabled on the Storage Account by following below steps. 

1. Go to ASC Resource Explorer
2. Select customer's storage account
3. Under configuration, verify if "Identity-based Directory Service for Azure File Authentication" property is set to AD.(Note: Value "AAD" means customer has Azure AD Auth setup on their account and this troubleshooter does not apply to that topic.)