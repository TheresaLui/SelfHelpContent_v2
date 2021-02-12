<properties
    pageTitle="Enforce 'Add or replace a monitor production VM' using Azure Policy"
    description="Azure Policy will help define, assign and manage standards for resources in your environment. This specific policy allows for resources to be tagged or for tagged to be replaced."
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="798cff57-b65c-4460-a069-87752458a948_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"	
    ownershipId="CGA_DataPlatform"
/>
# Add VM Monitor to your production VM
---
{
    "recommendationOfferingId": "c3c3299d-ee34-4610-844d-3782d691a7fe",
     "recommendationOfferingName": "Azure Advisor",
     "$schema": "AdvisorRecommendation",
     "recommendationTypeId": "a15a8fbc-22ac-41af-9039-2c9c4a7128e0",
     "dataSourceMetadata": {
        "schemaVersion": 2.0,
        "dataSource": "SAS"
     },
     "recommendationCategory": "OperationalExcellence",
     "recommendationImpact": "High",
     "recommendationResourceType": "Microsoft.Compute/virtualMachines",
     "recommendationFriendlyName": "AddMonitorProdVM",
     "recommendationMetadataState": "Active",
     "portalFeatures": [],
     "owner": {
        "email": "cga-sup@microsoft.com",
        "icm": {
            "routingId": "MDM://CGAAdvisorRecommendations",
            "service": "CGA Data Science",
            "team": "CGAAdvisorRecommendations"
        },
        "serviceTreeId": "0dbc6a29-122a-4ab5-8070-5868a2bcd57b"
     },
      "ingestionClientIdentities": [
        "397d7011-8a0c-4165-a3f5-8d4e5f2e676d"
      ],
      "recommendationTimeToLive": 86400,
      "version": 4.0,
      "learnMoreLink": "https://docs.microsoft.com/azure/azure-monitor/insights/vminsights-overview",
      "description": "Add Azure Monitor to your virtual machine (VM) labeled as production",
      "longDescription": "Azure Monitor for VMs monitors your Azure virtual machines (VM) and virtual machine scale sets at scale. It analyzes the performance and health of your Windows and Linux VMs,  and it monitors their processes and dependencies on other resources and external processes. It includes support for monitoring performance and application dependencies for VMs that are hosted on-premises or in another cloud provider.",
      "potentialBenefits": " Azure Monitor analyzes performance, health, and processes on your Windows and Linux VMs",
      "actions": [
            {
                "actionId": "99af20b1-297a-458f-822b-fd57787bc433",
                "description": "Add Azure Monitor to your virtual machine (VM) labeled as production",
                "actionType": "Blade",
                "extensionName": "Microsoft_Azure_WorkloadInsights",
                "bladeName": "VmResourceInsightsBladeViewModel",
                "metadata": {
                     "virtualMachineResourceId": "{resourceId}",
                     "sourceType": "Advisor.Recommendation"
                }
            }
      ],
      "resourceMetadata": {
	    "action": {
		"actionId": "d09035a6-5e17-4ecf-b70a-b5fd4479eb88",
		"actionType": "Blade",
		"extensionName": "HubsExtension",
		"bladeName": "ResourceMenuBlade",
		"metadata": {
			"id": "{resourceId}"
		    }
	    }
	  },
     "displayLabel": " Add Azure Monitor to your virtual machine (VM) labeled as production",
     "additionalColumns": [],
     "tip": "Azure Monitor analyzes performance, health, and processes on your Windows and Linux VMs"
}
---
