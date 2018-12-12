<properties
    authorAlias="v-anreg"
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
The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> with Enterprise Security Package
failed to deploy as the LDAP certificate is not configured correctly.
<!--/issueDescription-->

To secure the communication with  Azure Active Directory, configuration of secure LDAP is required for an Azure Active Directory Domain Services managed domain.

## **Recommended Steps**

**Create a self-signed certificate for secure LDAP**

**Note:** Please make sure you are using <!--$DomainName-->[DomainName]<!--/$DomainName--> and not using <!--$IpAddress-->[IpAddress]<!--/$IpAddress--> as the LDAPS URL while creating the cluster before following the steps given below:

1. On your Windows computer, open a new PowerShell window as Administrator and type the following commands, to create a new self-signed certificate
   
   **$lifetime=Get-Date**
   
   **New-SelfSignedCertificate -Subject <!--$DomainName-->[DomainName]<!--/$DomainName-->** `
   
   **-NotAfter $lifetime.AddDays(365) -KeyUsage DigitalSignature, KeyEncipherment** `
   
   __-Type SSLServerAuthentication -DnsName *.<!--$DomainName-->[DomainName]<!--/$DomainName-->, <!--$DomainName-->[DomainName]<!--/$DomainName-->__
   
 2. The newly created self-signed certificate is placed in the local machine's certificate store

## **Recommended Documents**

* [Configure a HDInsight cluster with Enterprise Security Package by using Azure Active Directory Domain Services](https://docs.microsoft.com/azure/hdinsight/domain-joined/apache-domain-joined-configure-using-azure-adds)
* [Configure secure LDAP (LDAPS) for an Azure AD Domain Services managed domain](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-configure-secure-ldap)
