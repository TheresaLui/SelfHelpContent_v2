<properties
    pageTitle="HDInsight AD DS Authentication Failure"
    description="HDInsightDomainUsersAuthenticationFailure"
    infoBubbleText="Found recent authentication failure for domain users. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    ms.author="v-anreg"
    displayOrder=""
    articleId="Hdi_AuthenticationFailure_DomainUsers"
    diagnosticScenario="HDInsightDomainUsersAuthenticationFailureInsight"
    selfHelpType="rca"
    supportTopicIds="32636420"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
There is a problem with the on-premises Active Directory instance for your HDInsight cluster: the **AllowCloudPasswordValidation** policy has not been set by the tenant. The administrator of the Azure Active Directory (AAD) tenant should update settings to allow the use of password hashes for Active Directory Federation Services (ADFS) backed users. 
<!--/issueDescription-->

## **Recommended Steps** 

To setup the **AllowCloudPasswordValidation** policy, follow the commands in the documentation for [Azure Active Directory Domain Services](https://docs.microsoft.com/azure/hdinsight/domain-joined/apache-domain-joined-architecture#set-up-different-domain-controllers).

## **Recommended Documents**

* [Azure Active Directory Domain Services](https://docs.microsoft.com/azure/hdinsight/domain-joined/apache-domain-joined-architecture#set-up-different-domain-controllers)
* [Configure Authentication For Federated Users Portal](https://docs.microsoft.com/azure/active-directory/manage-apps/configure-authentication-for-federated-users-portal)
* [Synchronization in an Azure AD Domain Services managed domain](https://docs.microsoft.com/azure/active-directory-domain-services/synchronization)
