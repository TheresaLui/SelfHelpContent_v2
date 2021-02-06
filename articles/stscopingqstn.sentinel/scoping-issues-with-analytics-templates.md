<properties
	pageTitle="Azure Sentinel - Analytic rules  - Issues with analytics templates"
	description="Azure Sentinel - Analytic rules  - Issues with analytics templates"
	authors="yaronsahar-ms"
	ms.author="yaronsahar"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32786018"
    productPesIds="16690"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping-issues-with-analytics-templates"
	schemaVersion="1"
	ownershipId="Azure_Sentinel"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Issues with analytics templates",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Provide any screenshots that are relevant to your issue",
                "formElements": [{
                "id": "AlertRuleID",
                "order": 4,
                "controlType": "textbox",
                "displayLabel": "Provide the Alert rule ID:",
                "required": true
                },{
                "id": "TemplateName",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "Provide the template name",
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
