<properties
pageTitle="Top common problems for "
description="Menu based workflow document for top compute problems"        
service=""
resource=""
ms.author=""
displayOrder=""
articleId=""
selfHelpType=""
resourceTags=""
productPesIds=""
cloudEnvironments=""
ownershipId=""
/>
# Diagnose and solve v2 sample article 
---
{
	"$schema":"SelfHelpContent",
	"commonProblems": [
		{				    
			"id": "Sample_common_problem_title_1",
			"title": "Sample common problem title 1",
			"description": "Sample common problem description 1",
			"category": "Deployment",
			"searchTags": "searchTag1, searchTag2, searchTag3",
			"supportTopicId": "",
			"subProblems":[
				{
					"title": "Sample common subproblem title 1",
					"description": "Sample common subproblem description 1",									
					"supportTopicId": "32628252",
					"commonSolutionArticleId": "9c0b9ec9-a07a-40e3-a6a2-f4d49f5f4ccb",
					"symptomId": "DeploymentFailuresAzurePortalInsight"
				},
				{
					"title": "Sample common subproblem title 2",
					"description": "Sample common subproblem description 2",										
					"supportTopicId": "32628252",
					"commonSolutionArticleId": "9c0b9ec9-a07a-40e3-a6a2-f4d49f5f4ccb",
					"symptomId": "DeploymentFailuresAzurePortalInsight"
				}
			]
		},			
		{			         
			"id": "Sample_common_problem_title-2",
			"title": "Sample common problem title 2",
			"description": "Sample common problem description 1",
			"category": "Connectivity",
			"searchTags": "searchTag1, searchTag2, searchTag3",
			"supportTopicId": "32628284",
			"commonSolutionArticleId": "0c333e4e-a865-4822-84b4-0c8eba727ffe",
			"symptomId": "cannotrdpazureportalinsight2"
		}		
	],
	"troubleshootingTools": [{			        				        
			"id": "Troubleshooting_tools_sample_title 1",
			"title": "Troubleshooting tools sample title 1",
			"description": "Troubleshooting tools sample description 1",			
			"category": "Connectivity",
			"searchTags": "searchTag1, searchTag2, searchTag3",
			"type": "tool",		
			"bladeLink": {				
				"extensionName": "Microsoft_Azure_Compute",
				"bladeName": "VirtualMachineRedeployViewModel",
				"parameters": [{
					"name": "id",
					"value": "$resourceId"
				}]
			}
		},
		{			        				        
			"id": "Troubleshooting_tools_sample_title 2",
			"title": "Troubleshooting tools sample title 2",
			"description": "Troubleshooting tools sample description 2",			
			"category": "Connectivity",
			"searchTags": "searchTag1, searchTag2, searchTag3",
			"type": "tool",		
			"bladeLink": {				
				"extensionName": "Microsoft_Azure_Compute",
				"bladeName": "VirtualMachineRedeployViewModel",
				"parameters": [{
					"name": "id",
					"value": "$resourceId"
				}]
			}
		}		
	]
}
---
