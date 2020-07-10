<properties
	pageTitle="How to manage access permissions to bot"
	description="Scoping questions to capture more details about issues encountered while managing access permissions to bot"
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688646"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="7F6D3CDB-F131-4CC0-AFAD-B96293DC47C9"
	ownershipId="Compute_BotService"
/>
# How to manage access permissions to bot 
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "How to manage access permissions to bot",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false
        },
		{
			"id": "new_bot",
			"order": 3,
			"controlType": "radioButtonGroup",
			"displayLabel": "Are you seeking assistance for an existing bot or for a new bot?",
			"radioButtonOptions": [{
					"value": "NewBot",
					"text": "A new bot"
				}, {
					"value": "ExistingBot",
					"text": "An existing Bot"
				}
			],
			"required": true
		},
		{
            "id": "RBAC_details",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "If you are making use of custom RBAC for roles and permissions, please provide the list of roles assigned to the user.",
            "required": false,
	    "watermarkText": "Please use the command shown in the info balloon.",
	    "infoBalloonText": "```az role assignment list --all --assignee example@example.com --output json | jq '.[] | {'principalName':.principalName,'roleDefinitionName':.roleDefinitionName,'scope':.scope} ``` For more guidance, read this <a href='https://docs.microsoft.com/azure/role-based-access-control/role-assignments-list-cli#list-role-assignments-for-a-user'>link</a>"
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide any additional details, if you see an error message list it or you are looking for specific guidance, explain that.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide as much details as possible"
        }
	]
}
---
