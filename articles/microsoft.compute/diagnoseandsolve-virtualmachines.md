<properties
pageTitle="Top common problems for compute"
description="Menu based workflow document for top compute problems"        
service="microsoft.compute"
resource="virtualmachines"
authors="gansmore"
ms.author="ganesh.more"
displayOrder=""
articleId="7bd33a4a-8d59-4f16-a965-f1ac9deb730e"
selfHelpType="diagnoseandsolve"
resourceTags="linux, ubuntu"
productPesIds="15571"
cloudEnvironments="public"
/>
# Diagnose and solve v2 test article 
---
{
	"$schema":"SelfHelpContent",
	"commonProblems": [{				    
			"title": "I can't connect to my virtual machine",
			"description": "Discover issues that may be affecting connectivity to your VM due to either  platform issue or VM issue",
			"category": "Connectivity",
			"searchTags": "connectivity, rdp",
			"supportTopicId": "32615525",
			"subProblems":[{
					"title": "My configuration change impacted connectivity",
					"description": "My configuration change impacted connectivity",										
					"supportTopicId": "32615530",
					"commonSolutionArticleId": "d530b6fe-3096-40c1-9ef0-2bc37364bee5",
					"symptomId": "cannotrdpazureportalinsight"
				},
				{
					"title": "Troubleshoot my VM firewall",
					"description": "Troubleshoot my VM firewall",										
					"supportTopicId": "32615534",
					"commonSolutionArticleId": "d530b6fe-3096-abcd-9ef0-2bc37364abcd",
					"symptomId": "computelivesiterca"
				}
			]
		}, {			         
			"title": "I can't reboot/restart my virtual machine",
			"description": "Discover issues that may be affecting connectivity to your VM due to either  platform issue or VM issue",
			"category": "Connectivity",
			"searchTags": "restart, reboot",
			"supportTopicId": "4354354565",
			"commonSolutionArticleId": "d530b6fe-3096-40c1-9ef0-2bc37364bee5",
			"symptomId": "cannotrdpazureportalinsight"
		},
		{				    
			"title": "My virtual machine is running slow",
			"description": "Discover issues that may be affecting connectivity to your VM due to either  platform issue or VM issue",
			"category": "Performance",
			"commonSolutionArticleId": "d530b6fe-3096-abcd-9ef0-2bc37364abcd",
			"searchTags": "performance, vm",			
			"supportTopicId": "4354354565"				    
		}, 
		{				    
			"title": "How do I reset password of my virtual machine?",
			"description": "Discover issues that may be affecting connectivity to your VM due to either  platform issue or VM issue",
			"category": "Reset",
			"commonSolutionArticleId": "",
			"supportTopicId": "4354354565"
		}
	],
	"troubleshootingTools": [{			        				        
			"title": "Redeploy virtual machine",
			"description": "Migrate this virtual machine to a different host to resolve connectivity issues",
			"newTagExpiryDate": "4/14/2019",
			"category": "Connectivity",
			"searchTags": "deployment, rdp", 
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
			"title": "Can't connect to virtual machine",
			"description": "Discover issues that may be affecting connectivity to your VM due to either  platform issue or VM issue",
			"newTagExpiryDate": "",
			"type": "insight",
			"searchTags": "connectvity, rdp",
			"category": "Connectivity",
			"supportTopicId": "4354354565",
			"symptomId": "cannotrdpazureportalinsight"
		}
	]
}
---
