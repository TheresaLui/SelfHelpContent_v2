<properties
pageTitle="Top common problems for storage"
description="Menu based workflow document for top storage problems"        
service="microsoft.storage"
resource="storageaccounts"
ms.author="leakkari"
displayOrder=""
articleId="024fb399-f39d-41b4-a649-a45d5fdad483"
selfHelpType="diagnoseandsolve"
resourceTags=""
productPesIds="15629,16459,16598,16460,16461,16462"
cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
ownershipId="StorageMediaEdge_AccountManagement"
/>
# Diagnose and solve v2 article for Storage
---
{
	"$schema":"SelfHelpContent",
	"commonProblems": [
		{
			"id": "cannot_change_replication_type",
			"title": "Cannot change account replication type",
			"description": "Cannot change account replication type",
			"category": "Replication",
			"searchTags": "replication, change, lrs, grs, ragrs, zrs, gzrs, ragzrs",
			"supportTopicId": "32691089",
			"commonSolutionArticleId": "commonSoln_replication",
			"symptomId": ""
		}
	],
	"troubleshootingTools": [
		{
			"id": "Storage_Account_Health_tool",
			"title": "Storage Account Health",
			"description": "Use Azure Resource health to diagnose any issues with the resource. It monitors and indicates any availability issues.",
			"category": "Management",
			"searchTags": "resource health, availability, connectivity, Health",
			"type": "tool",
			"bladeLink": {
				"extensionName": "Microsoft_Azure_Health",
				"bladeName": "ResourceHealthDetailBlade",
				"parameters": [
					{
						"name": "resourceId",
						"value": "$resourceId"
					}
				]
			}
		},
		{
			"id": "Azure_Service_Health_tool",
			"title": "Azure Service Health",
			"description": "Use the Azure Service Health blade to learn about current service issues that may affect your resources",
			"category": "Management",
			"searchTags": "outage, Azure issues, production, platform impact",
			"type": "tool",
			"bladeLink": {
				"extensionName": "Microsoft_Azure_Health",
				"bladeName": "ServiceIssuesBlade",
				"parameters": [
					{
						"name": "id",
						"value": "$resourceId"
					}
				]
			}
		}
	]
}
---
