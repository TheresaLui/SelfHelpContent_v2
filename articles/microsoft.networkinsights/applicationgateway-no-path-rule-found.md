<properties
	pageTitle="Application Gateway - No Path Rule Found. Getting Defaults"
	description="Application Gateway - Rule is path-based but no path rules matched in URL path map."
	infoBubbleText="Rule is path-based but no path rules matched in the URL path map. See details on the right."
	service="microsoft.network"
	resource="Application Gateway"
	authors="cgeisbush"
	ms.author="chgeis"
	displayOrder="1"
	articleId="AppGwNoPathRuleFoundInsight"
	diagnosticScenario="AppGwChecklistInsights"
	selfHelpType="diagnostics"
	supportTopicIds="32436961,32573483,32582834"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# We have detected a potential issue with a path-based rule configured on your Application Gateway

<!--issueDescription-->
We have detected a potential issue with a path-based routing rule configured on your Application Gateway.
<!--/issueDescription-->

- **Application Gateway:** <!--$GatewayName-->Application Gateway<!--/$GatewayName-->
- **Rule Name:** <!--$RuleName-->Rule Name<!--/$RuleName-->
- **URL Path:** <!--$UrlPath-->URL Path<!--/$UrlPath-->
- **URL Path Map Name:** <!--$UrlPathMapName-->URL Path Map Name<!--/$UrlPathMapName-->

Typically, when we utilize a path-based routing rule, we expect to utilize URLs that will match to a path in the map.  However, URL (<!--$UrlPath-->URL Path<!--/$UrlPath-->) did not match any paths in the map.  When no match is found, Application Gateway uses the default path configured on the routing rule.

If you experience path-routing issues, review the URL path map (<!--$UrlPathMapName-->URL Path Map Name<!--/$UrlPathMapName-->) configuration for your routing rule (<!--$RuleName-->Rule Name<!--/$RuleName-->).

## **Recommended Documents**

* [Create an application gateway with path-based routing rules using the Azure portal](https://docs.microsoft.com/azure/application-gateway/application-gateway-create-url-route-portal)
