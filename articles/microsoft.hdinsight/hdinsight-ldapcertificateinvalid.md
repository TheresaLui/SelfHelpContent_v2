<properties
    pageTitle="LDAP certificate invalid"
    description="InvalidLdapCertificateIssue"
    infoBubbleText="Found recent LDAP certificate issue. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    displayOrder=""
    articleId="Hdi_Crud_ConfigureLdap"
    diagnosticScenario="HDInsightLdapCertificateInvalidInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32511166, 32588500, 32588501, 32588502"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> 
failed to deploy as LDAP certificate is not configured correctly.
<!--/issueDescription-->

Configuration of secure LDAP is required for an Azure AD Domain Services managed domain.

## **Recommended Steps**

Create a self-signed certificate for secure LDAP

1. Open a new PowerShell window as Administrator and type the following commands, to create a new self-signed certificate.
2. $lifetime=Get-Date
New-SelfSignedCertificate -Subject <!--$DomainName-->[DomainName]<!--/$DomainName--> `
  -NotAfter $lifetime.AddDays(365) -KeyUsage DigitalSignature, KeyEncipherment `
  -Type SSLServerAuthentication -DnsName *.<!--$DomainName-->[DomainName]<!--/$DomainName-->, <!--$DomainName-->[DomainName]<!--/$DomainName--> <br>
 3. The newly created self-signed certificate is placed in the local machine's certificate store.

## **Recommended Documents**

* [Configure secure LDAP (LDAPS) for an Azure AD Domain Services managed domain](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-configure-secure-ldap)
