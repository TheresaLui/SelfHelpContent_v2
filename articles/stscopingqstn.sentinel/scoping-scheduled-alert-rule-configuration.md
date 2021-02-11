<properties
	pageTitle="Azure Sentinel - Analytic rules  - Scheduled alert rule  - Configuration"
	description="Azure Sentinel - Analytic rules  - Scheduled alert rule  - Configuration"
	authors="yaronsahar-ms"
	ms.author="yaronsahar"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32786020"
    productPesIds="16690"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping-scheduled-alert-rule-configuration"
	schemaVersion="1"
	ownershipId="Azure_Sentinel"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Scheduled alert rule  - Configuration",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Provide any screenshot that may be relevant to your issue",
                "formElements": [{
                "id": "AlertRuleID",
                "order": 4,
                "controlType": "textbox",
                "displayLabel": "Provide the Alert rule ID:",
                "required": true
                },{
                "id": "ConfigSet",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "What kind of configuration you are trying to set?",
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
