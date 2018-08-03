<properties
	pageTitle="Application Gateway - potential issue with path rule detected"
	description="Application Gateway - potential issue with path rule detected.  Trailing slash detected in path rule"
	infoBubbleText="Potential issue with path rule detected.  Trailing slash detected in path rule. See details on the right."
	service="microsoft.network"
	resource="Application Gateway"
	authors="cgeisbush"
	displayOrder="1"
	articleId="AppGwPathRuleHasTrailingSlashInsight"
	diagnosticScenario="AppGwChecklistInsights"
	selfHelpType="diagnostics"
	supportTopicIds="32436961,32573483,32582834"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public"
/>

# We have detected a potential issue with a path-based rule configured on your Application Gateway

<!--issueDescription-->
We have detected a potential issue with a path-based routing rule configured on your Application Gateway.

- **Application Gateway:** <!--$GatewayName-->Application Gateway<!--/$GatewayName-->

A rule exists for path **<!--$Path-->Path<!--/$Path-->**, however the Application Gateway URL provided upon creation of your support request contains path **<!--$UrlPath-->UrlPath<!--/$UrlPath-->**.

The presence of a trailing slash (/) in your path may cause undesired path routing.
<!--/issueDescription-->

If you experience path-routing issues, try removing the trailing slash from your path-based rule.

For help on creating and editing path-based routing rules, you can refer to the article "[Create an application gateway with path-based routing rules using the Azure portal](https://docs.microsoft.com/azure/application-gateway/application-gateway-create-url-route-portal)"
