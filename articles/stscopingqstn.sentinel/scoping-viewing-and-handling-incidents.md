<properties
	pageTitle="Azure Sentinel - Incidents and investigation - Viewing and handling incidents"
	description="Azure Sentinel - Incidents and investigation - Viewing and handling incidents"
	authors="yaronsahar-ms"
	ms.author="yaronsahar"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32786000"
    productPesIds="16690"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping-viewing-and-handling-incidents"
	schemaVersion="1"
	ownershipId="Azure_Sentinel"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Viewing and handling incidents",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Please provide any screenshot that may be relevant to your issue",
                "formElements": [{
                "id": "AlertID",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "Please provide the SystemAlertId of the relevant alert:",
                "required": true
                },{
                "id": "AlertRuleID",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "Please provide the alert rule ID of the relevant analytic rule:",
                "required": false
                },{
                "id": "ProductName",
                "order": 4,
                "controlType": "textbox",
                "displayLabel": "What is the procut for which the incidents was not created?",
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
