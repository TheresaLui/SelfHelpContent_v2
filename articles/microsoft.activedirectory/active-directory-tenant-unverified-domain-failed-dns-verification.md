<properties
	pageTitle="Failed DNS Verification Customer Ready Content"
	description="DNS Verification was not successful for the domain"
	infoBubbleText="See details on the right"
	service="microsoft.activedirectory"
	resource=""
	authors="bernawy"
	ms.author="bernaw"
	displayOrder="4"
	articleId="Tenant_Unverified_Domain_Failed_DNS_Verification"
	diagnosticScenario="FailedDNSVerification"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_B2B"
/>

# DNS Verification was not successful for the domain
<!--/issueDescription-->
We are unable to successfully confirm registration of the domain verification records in DNS. We queried DNS for the TXT record at <!--$domain-->[domain]<!--/$domain--> and did not find an entry matching the required verification record <!--$txtRecord-->[txtRecord]<!--/$txtRecord-->.
<!--/issueDescription-->

## **Recommended Steps**

1. Wait one hour. This will allow your DNS records to propagate at your domain name registrar (such as GoDaddy) before Azure AD can verify the domain. This process can take an hour or more.
2.	Ensure the DNS record was entered, and that it is correct. Complete this step at the website for the domain name registrar for the domain (for example it may be a registrar like GoDaddy, Namecheap). Azure AD cannot verify the domain name if:

    - The DNS entry is not present in the DNS zone file
    - It is not an exact match with the DNS entry that Azure AD provided you

If you do not have access to update DNS records for the domain at the domain name registrar, share the DNS entry with the person or team at your organization who has this access, and ask them to add the DNS entry.

## **Recommended Documents**

* [Custom Domain Troubleshooting](https://docs.microsoft.com/azure/active-directory/add-custom-domain#troubleshooting)
