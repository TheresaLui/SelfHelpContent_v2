<properties
	pageTitle="Azure Sentinel - Analytic rules  - Entities in scheduled alert rule"
	description="Azure Sentinel - Analytic rules  - Entities in scheduled alert rule"
	authors="yaronsahar-ms"
	ms.author="yaronsahar"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32786012"
    productPesIds="16690"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping-entities-in-scheduled-alert-rule"
	schemaVersion="1"
	ownershipId="Azure_Sentinel"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Entities in scheduled alert rule",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Provide any screenshot relevant to your issue",
                "formElements": [{
                "id": "AlertRuleID",
                "order": 4,
                "controlType": "textbox",
                "displayLabel": "Provide the Alert rule ID:",
                "required": true
                },{
                "id": "MissingEntAlertID",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "Provide the Alert ID where the entities are not set:",
                "required": false
                                                },{"id": "problem_description",
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
