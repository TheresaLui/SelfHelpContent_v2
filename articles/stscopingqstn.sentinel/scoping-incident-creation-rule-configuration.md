<properties
	pageTitle="Azure Sentinel - Analytic rules  - Incident creation rule - Configuration"
	description="Azure Sentinel - Analytic rules  - Incident creation rule - Configuration"
	authors="yaronsahar-ms"
	ms.author="yaronsahar"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32786016"
    productPesIds="16690"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping-incident-creation-rule-configuration"
	schemaVersion="1"
	ownershipId="Azure_Sentinel"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Incident creation rule - Configuration",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Please provide any screenshots that are relevant to your issue",
                "formElements": [{
                "id": "AlertRuleID",
                "order": 4,
                "controlType": "textbox",
                "displayLabel": "Provide the Alert rule ID:",
                "required": true
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
