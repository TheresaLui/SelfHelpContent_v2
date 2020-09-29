<properties
    pageTitle="User gets prompted for credentials while running net use command"
    description="User gets prompted for credentials while running net use command"
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
    articleId="96e27dd6-4181-4537-a0cc-3492d50f353b"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# User gets prompted for credentials while running net use command

**Symptoms**

The user attempts to mount and gets prompted for credentials.  The user may or may not proceed to type in their credentials and get an error like "the username or password is incorrect"

**How to Detect**

Due to issues within a customer's domain environment, clients may have trouble getting Kerberos tickets to the storage account. Please have the customer run the following command for their storage account. 

**klist get cifs/<storageaccount>.file.core.windows.net**