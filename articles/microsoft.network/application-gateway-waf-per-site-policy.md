<properties
	pageTitle="Application Gateway WAF Per-site Policy"
	description="Application Gateway WAF Per-site Policy"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32691039"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="appgw-waf-ip-reputation"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway WAF Per-site policy

With per-site WAF policies, you can protect multiple sites with differing security needs behind a single WAF by using per-site policies. For example, if there are five sites behind your WAF, you can have five separate WAF policies (one for each listener) to customize the exclusions, custom rules, managed rule sets, and all other WAF settings for each site.

Say your application gateway has a global policy applied to it. Then you apply a different policy to a listener on that application gateway. The listener's policy now takes effect for just that listener. The application gateway’s global policy still applies to all other listeners and path-based rules that don't have a specific policy assigned to them.

## **Recommended Documents**

* [Configure per-site WAF policy for Application Gateway using Azure PowerShell](https://docs.microsoft.com/azure/web-application-firewall/ag/per-site-policies)
* [Application Gateway WAF Per-site Policy overview](https://docs.microsoft.com/azure/web-application-firewall/ag/policy-overview#per-site-waf-policy)
