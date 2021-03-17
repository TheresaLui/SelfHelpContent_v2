<properties
	pageTitle="Azure Sentinel - Data collection - Connectors based on REST API,  Azure Functions or custom logs"
	description="Azure Sentinel - Data collection - Connectors based on REST API,  Azure Functions or custom logs"
	authors="yaronsahar-ms"
	ms.author="yaronsahar"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32786003"
    productPesIds="16690"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping-connectors-based-on-restapi-azure-fnctions-or-custom-logs"
	schemaVersion="1"
	ownershipId="Azure_Sentinel"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Connectors based on REST API,  Azure Functions or custom logs",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Attach a screenshot of the relevant Connector blade",
                "formElements": [{
                "id": "ConnectorName",
                "order": 4,
                "controlType": "textbox",
                "displayLabel": "What is the data connector name?",
                "required": true
				 },{
				"id": "AnyIssue",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "Is there any data latency, duplication and/or missing data?",
                "required": false
				 },{
				"id": "problem_description",
				"order": 1,
				"controlType": "multilinetextbox",
				"displayLabel": "Description",
				"useAsAdditionalDetails": true,
				"required": true
				},{
				"id": "problem_start_time",
				"order": 8,
				"controlType": "datetimepicker",
				"displayLabel": "When did the problem start?",
				"required": true
                  }]
}
---