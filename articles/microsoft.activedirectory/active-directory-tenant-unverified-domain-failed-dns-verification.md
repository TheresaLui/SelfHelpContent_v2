<properties
	pageTitle="Failed DNS Verification Customer Ready Content"
	description="DNS Verification was not successful for the domain"
	infoBubbleText=""
	service="microsoft.activedirectory"
	resource=""
	authors="bernawy"
	displayOrder="4"
	articleId="Tenant_Unverified_Domain_Failed_DNS_Verification"
	diagnosticScenario="FailedDNSVerification"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# DNS Verification was not successful for the domain
Hi {customerName},

I have found some information regarding your service request [{srNumber}]. We are unable to successfully confirm registration of the domain verification records in DNS. We queried DNS for the TXT record at [{domain]} and did not find an entry matching the required verification record {txtRecord}].

The recommended steps for you are noted below: 
1.	Please wait an hour. This will allow your DNS records to propagate at your domain name registrar (such as GoDaddy) before Azure AD can verify the domain. This process can take an hour or more.

2.	Ensure the DNS record was entered, and that it is correct. Complete this step at the website for the domain name registrar for the domain (for example it may be a registrar like GoDaddy, Namecheap). Azure AD cannot verify the domain name if:
    - The DNS entry is not present in the DNS zone file.
    - It is not an exact match with the DNS entry that Azure AD provided you. 

If you do not have access to update DNS records for the domain at the domain name registrar, share the DNS entry with the person or team at your organization who has this access, and ask them to add the DNS entry.

Supporting Links: https://docs.microsoft.com/en-us/azure/active-directory/add-custom-domain#troubleshooting

I will be more than happy to assist you with the steps if needed.

Thank you,<br>
{engineerName}