<properties
    pageTitle="Microsoft internal customer wants to enable AD Auth on their storage account"
    description="Microsoft internal customer wants to enable AD Auth on their storage account"
    infoBubbleText="Microsoft internal customer wants to enable AD Auth on their storage account"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="Diagnostics"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="a4f4ecfe-3983-4da8-990c-e27e887892b2"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Microsoft internal customer wants to enable AD Auth on their storage account

<!--issueDescription-->
Microsoft internal customer wants to enable AD Auth on their storage account. They are facing an issue when they are trying to run Join-AzStorageAccountForAuth command.
<!--/issueDescription-->
## **Recommended Action**

Users which are part of the Microsoft tenant and have Azure Subscription in Microsoft AAD can join their storage account to On Prem Active Directory if they create a Computer Object. 

Users won't have permissions to create a computer object without specifying the Organizational Unit.  REDMOND(Microsoft) policy doesn't let users create objects anywhere, users must create it in a supported Organizational Unit.

Ask the user to try running the following Join command.Change the domain as needed:

    Join-AzStorageAccountForAuth -Domain "redmond.corp.microsoft.com" -DomainAccountType ComputerAccount -OrganizationalUnitDistinguishedName "OU=Workstations,OU=Machines,DC=redmond,DC=corp,DC=microsoft,DC=com" -Name $StorageAccountName -ResourceGroupName $ResourceGroupName -Verbose
