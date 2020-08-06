<properties
    pageTitle="Problems configuring location-based conditional access"
    description="Problems configuring location-based conditional access"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jcardena"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="conditionalaccess_overview"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="5b282ff7-5a29-493b-a40e-4d5be32b8303"
	ownershipId="AzureIdentity_User"
/>

# Problems configuring location-based conditional access

You can tie conditional access policies to the location of the client you have used to connect to Azure Active Directory. The follow options are available: <br>

*	Configure the [trusted IP ranges](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next#trusted-ips) for your company, in Azure AD <br>
*	Use the ADFS [inside corpnet claim](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-adfs-cloud) to indicate the user is on the corporate network.

The location condition of a conditional access policy enables you to apply policy to locations that are not on a trusted network. You can do this by setting a policy condition that includes **All locations**, which means from anywhere, and exclude **All trusted IPs**. 
<br><br>
For more details, see:
<br>
[How to configure "at work" networks for conditional access](http://aka.ms/calocation) <br>
[How to configure Trusted IP ranges in Azure AD](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next#trusted-ips) <br>
[How to configure the ADFS inside corporate network claim](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-adfs-cloud)