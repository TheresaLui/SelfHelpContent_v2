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
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue

There is a problem with the on-premises Active Directory instance for your HDInsight cluster: the `AllowCloudPasswordValidation` policy has not been set by the tenant. The Company Administrator of the Azure Active Directory (AAD) tenant should run the following commands to enable AAD to use password hashes for Active Directory Federation Services (ADFS) backed users. <br>

## **Recommended Steps** 

1. Install the Azure AD PowerShell module with `Install-Module AzureADPreview`
2. Enter Connect-AzureAD by using global administrator (tenant administrator) credentials
3. Check if the Microsoft Azure PowerShell service principal has already been created: `$powershellSPN = Get-AzureADServicePrincipal -SearchString "Microsoft Azure Powershell"`
4. If it doesn't exist (that is, if (`$powershellSPN -eq $null`)), create the service principal: `$powershellSPN = New-AzureADServicePrincipal -AppId 1950a258-227b-4e31-a9cf-717495945fc2`
5. Create and attach the policy to this service principal": 

```
$policy = New-AzureADPolicy -Definition @("{`"HomeRealmDiscoveryPolicy`":{`"AllowCloudPasswordValidation`":true}}") -DisplayName EnableDirectAuth -Type HomeRealmDiscoveryPolicy

Add-AzureADServicePrincipalPolicy -Id $powershellSPN.ObjectId -refObjectID $policy.ID
```

## **Recommended Documents**

* [Azure Active Directory Domain Services](https://docs.microsoft.com/azure/hdinsight/domain-joined/apache-domain-joined-architecture#set-up-different-domain-controllers)
