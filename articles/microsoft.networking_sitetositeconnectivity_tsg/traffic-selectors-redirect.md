﻿<properties
	pageTitle="Check for traffic selector misconfiguration"
	description="Check for traffic selector misconfiguration"
	service="microsoft.network"
	resource="vpnGateways"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32591158,32584882,32584881"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="3f9efb16-ee1e-4ddb-bf0a-d5fd491d7ce5"
/>

# How to check for traffic selector misconfiguration

## **Recommended Steps**

* In this scenario, there are Traffic Selectors in place that are only allowing connectivity to certain subnets and not to others.
* Notice that usage of such limited traffic selectors may not prevent the VPN tunnel from correctly establishing, but will only block traffic from flowing.
* The traffic selectors may exist on the Azure configuration or the customer configuration.
* If you need to view Traffic Selector logs, review IkeLogs table in Kusto at the time of the issue.
* Please use the 'Start Over' button to restart this workflow and use the Resource Unreachable Traffic Selector path
