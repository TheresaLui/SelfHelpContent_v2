<properties
	pageTitle="Select the customer issue"
	description="Select the customer issue"
	service="microsoft.network"
	resource="vpnGateways"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32591158,32584882,32584881"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="2a4d7fcb-c61e-438b-a172-b9fda94b5ec0"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Select the customer issue

## **Recommended Steps**

While we begin troubleshooting this scenario, please consider the below points.

1. Go through the ASC insights and certainly browse through the **[emerging issues and known bugs](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/254656/Site-to-Site?anchor=active-site-to-site-work-items)** page to eliminate any known error.
2. Ensure there is no IP address overlap or mismatch, and the resources (Connection, Local Network Gateway, and VPN Gateway) are healthy. If any of the resources are in failed state, then troubleshoot the failed operation before you begin with this TSG.
3. Please provide us actionable feedback with supporting content and screenshots to make this TSG better.
4. If you reach a state where you need to escalate, it is recommended that you share _Network Traces_ from all the hops, including the ones from hosts, along with _Test Traffic_ logs, and _Effective Routes_ output.
