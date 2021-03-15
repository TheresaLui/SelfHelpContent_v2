<properties
	pageTitle="Azure Sentinel - Data collection - Connectors based on Logstash output plugin integration"
	description="Azure Sentinel - Data collection - Connectors based on Logstash output plugin integration"
	authors="yaronsahar-ms"
	ms.author="yaronsahar"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32786002"
    productPesIds="16690"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping-connectors-based-on-logstash-output-plugin-integration"
	schemaVersion="1"
	ownershipId="Azure_Sentinel"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Connectors based on Logstash output plugin integration",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Attach a screenshot of the relevant Connector blade",
                "formElements": [{
                "id": "LSConfig",
                "order": 4,
                "controlType": "textbox",
                "displayLabel": "Provide the Logstash configuration",
                "required": true
				 },{
				"id": "AnyIssue",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "Provide the Logstash log",
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
