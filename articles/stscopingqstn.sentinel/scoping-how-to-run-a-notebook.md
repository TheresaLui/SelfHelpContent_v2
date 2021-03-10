<properties
	pageTitle="Azure Sentinel - Threat Hunting ,Watchlist and Notebooks  - How to run a notebook"
	description="Azure Sentinel - Threat Hunting ,Watchlist and Notebooks  - How to run a notebook"
	authors="yaronsahar-ms"
	ms.author="yaronsahar"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32786013"
    productPesIds="16690"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping-how-to-run-a-notebook"
	schemaVersion="1"
	ownershipId="Azure_Sentinel"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "How to run a notebook ",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Please provide any screenshots that are relevant to your issue",
				"formElements": [{
                "id": "NotebookName",
                "order": 4,
                "controlType": "textbox",
                "displayLabel": "Can you please share the Notebook name you are attempting to run?",
                "required": true
                },{
				"id": "BadNetwork",
                "order": 5,
                "controlType": "textbox",
                "displayLabel": "Is the browser you are using behind a firewall?",
                "required": false
                },{
                "id": "BadNetwork2",
                "order": 6,
                "controlType": "textbox",
                "displayLabel": "Is websockets enabled by the firewall",
                "required": false
                },{
				"id": "RBACrole",
                "order": 7,
                "controlType": "textbox",
                "displayLabel": "Can you please share the RBAC role of the user?",
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