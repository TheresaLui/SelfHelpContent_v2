<properties
    pageTitle="Permission issues on AD DS Connector Account"
    description="Permission issues on AD DS Connector Account"
    infoBubbleText="Permission issues on AD DS Connector Account See details on the right."
    service="microsoft.aad.iam"
    resource="aadconnect"
    authors="rodejo"
    ms.author="rodejo"
    displayOrder="1"
    articleId="AADtoADSync_AADConnect_ASC_ADDSConnectorAccount_Permission_Issues"
    diagnosticScenario=""
    selfHelpType="Diagnostics"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="Identity_AuthReach_HybridAuth_ADFS"
/>
# Permission issues on AD DS Connector Account
<!--issueDescription-->
We noticed that there are issues with the account or the permissions that are assigned to the AD DS Connector Account. This is account that Azure AD Connect uses to connect to your Windows Server Active Directory. Due to these account or permissions issues Azure AD Connect cannot read and/or write data from or to your directory, the synchronization service does not run correctly and you may see incorrect or unexpected synchronization results and/or synchronization errors
<!--/issueDescription-->

## **Recommended Steps**

Verify that the AD DS Connector account and its permissions are configured and working correctly:

* Verify that the service account used to run synchronization service exists in your Active Directory 
* Verify that the service account password has not expired. It is recommended that the account should be configured with "password never expires" option. 
* Verify that the account has the required permissions to access your Active Directory objects  
* Ensure the service account has right permissions to log into Windows
* Check if any group policy is changing the permissions

## **Recommended Documents**

* [Configure AD DS Connector Account](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-configure-ad-ds-connector-account)