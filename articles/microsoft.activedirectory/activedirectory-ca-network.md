<properties
    pageTitle="How to use location and trusted IP in conditional access conditions"
    description="How to use location and trusted IP in conditional access conditions"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jcardena"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="conditionalaccess_overview"
    productPesIds=""
    cloudEnvironments="public"
/>

# How to use location and trusted IP in conditional access conditions

You have two options for setting trusted IP ranges for your organization. <br>

*	In Azure AD configure the trusted IP ranges for your company
*	Use the ADFS inside corpnet claim to indicate the user is on the corporate network.

After specifying trusted IP ranges, you can create conditional access policy that uses the location conditions. For an example a policy can be created to block application access when a user is not on at a trusted IP
<br>
The following documents can help you resolve some of the common issues in this category
<br>

[How to configure "at work" networks for conditional access](http://aka.ms/calocation) <br>
[How to configure Trusted IP ranges in Azure AD](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next#trusted-ips) <br>
[How to configure the ADFS inside corporate network claim](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-adfs-cloud)