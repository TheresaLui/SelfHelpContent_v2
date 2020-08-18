<properties
	pageTitle="Application Gateway WAF IP Reputation (Bot mitigation)"
	description="Application Gateway WAF IP Reputation (Bot mitigation)"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32691040"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="appgw-waf-ip-reputation"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# IP Reputation (Bot mitigation) with Application Gateway WAF

You can enable a managed bot protection rule set for your WAF to block or log requests from known malicious IP addresses. The IP addresses are sourced from the Microsoft Threat Intelligence feed. Intelligent Security Graph powers Microsoft threat intelligence and is used by multiple services including Azure Security Center.

You can use the Bot Protection ruleset alongside any of the OWASP rulesets (2.2.9, 3.0, and 3.1). Only one OWASP ruleset can be used at any given time. The bot protection ruleset contains an additional rule that appears in its own ruleset. It's titled Microsoft_BotManagerRuleSet_0.1, and you can enable or disable it like the other OWASP rules.

The bot mitigation ruleset list of known bad IP addresses updates multiple times per day from the Microsoft Threat Intelligence feed to stay in sync with the bots. Your web applications are continuously protected even as the bot attack vectors change.

## **Recommended Documents**

* [Configure bot protection for Web Application Firewall on Azure Application Gateway (Preview)](https://docs.microsoft.com/azure/web-application-firewall/ag/bot-protection)
* [Azure WAF on Application Gateway Bot protection overview](https://docs.microsoft.com/azure/web-application-firewall/ag/bot-protection-overview)
