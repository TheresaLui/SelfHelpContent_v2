<properties
	pageTitle="Azure Sentinel - Data collection - Connectors based on Windows agents"
	description="Azure Sentinel - Data collection - Connectors based on Windows agents"
	authors="yaronsahar-ms"
	ms.author="yaronsahar"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32786001"
    productPesIds="16690"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_WinAgentBased"
	schemaVersion="1"
	ownershipId="Azure_Sentinel"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Connectors based on Windows agents",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Please attach a screenshot of relevant Connector blade",
                "formElements": [
                {
                    "id": "Managed by Azure",
                    "order": 6,
                    "controlType": "dropdown",
                    "displayLabel": "Does you agent machine is managed by Azure?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Managed by Azure",
                            "text": "Managed by Azure"
                        },
                        {
                            "value": "Unmanaged by Azure",
                            "text": "Unmanaged by Azure"
                        },
	                    {
							"value": "dont_know_answer",
							"text": "None of the above"
						}
                    ],
                    "required": true
                }],{
                "id": "OSandAgent_version",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "Which OS and OMS version are you using?",
                "required": true
                },{
                "id": "ConnectorName",
                "order": 4,
                "controlType": "textbox",
                "displayLabel": "What connector are you using?",
                "required": true
                }
}
---
