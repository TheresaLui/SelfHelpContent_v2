<properties
	pageTitle="Create a bot channel registration"
	description="Scoping questions to capture more details about issues encountered while creating a bot channel registration"
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688635"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="2750A106-78C7-4B04-9C1D-379E5AE478D2"
	ownershipId="Compute_BotService"
/>
# Create a bot channel registration
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Create a bot channel registration",
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
            "id": "RBAC_details",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "If you are making use of custom RBAC for roles and permissions, please provide the list of roles assigned to the user.",
            "required": false,
	    "watermarkText": "Please use the command shown in the info balloon.",
	    "infoBalloonText": "```az role assignment list --all --assignee example@example.com --output json | jq '.[] | {'principalName':.principalName,'roleDefinitionName':.roleDefinitionName,'scope':.scope} ``` For more guidance, read this <a href='https://docs.microsoft.com/azure/role-based-access-control/role-assignments-list-cli#list-role-assignments-for-a-user'>link</a>"
        },
		{
			"id": "error_advice",
			"order": 4,
			"controlType": "radioButtonGroup",
			"displayLabel": "Are you seeing an error while creating the registration or are you looking for advice?",
			"radioButtonOptions": [{
					"value": "Error",
					"text": "Seeing an error"
				}, {
					"value": "Advice",
					"text": "Looking for advice"
				}
			],
			"required": true
		},
				{
			"id": "error_bothandle",
			"order": 5,
			"visibility":"error_advice == Error",
			"controlType": "textbox",
			"displayLabel": "Bot handle you used ",
			"required": false
		},
		{
			"id": "error_subscription",
			"order": 6,
			"visibility":"error_advice == Error",
			"controlType": "textbox",
			"displayLabel": "The subscription you used",
			"required": false
		},
		{
			"id": "error_rg",
			"order": 7,
			"visibility":"error_advice == Error",
			"controlType": "textbox",
			"displayLabel": "The name of the resource group you used",
			"required": false
		},
		{
			"id": "error_location",
			"order": 8,
			"visibility":"error_advice == Error",
			"controlType": "textbox",
			"displayLabel": "Enter the location you selected",
			"required": false
		},
		{
			"id": "error_pricing",
			"order": 9,
			"visibility":"error_advice == Error",
			"controlType": "textbox",
			"displayLabel": "The pricing tier you selected",
			"required": false
		},
		{
			"id": "error_endpoint",
			"order": 10,
			"visibility":"error_advice == Error",
			"controlType": "textbox",
			"displayLabel": "The messaging endpoint URL",
			"required": false
		},
		{
			"id": "error_appins",
			"order": 11,
			"visibility":"error_advice == Error",
			"controlType": "radioButtonGroup",
			"displayLabel": "Did you select App Insights?",
			"radioButtonOptions": [{
					"value": "error_yes",
					"text": "Yes"
				}, {
					"value": "error_no",
					"text": "No"
				}
			],
			"required": false
		},
		{
			"id": "error_appinsloc",
			"order": 12,
			"visibility":"error_appins == error_yes",
			"controlType": "textbox",
			"displayLabel": "The location for Application Insights you selected",
			"required": false
		},
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details, if you see an error message list it or you are looking for specific guidance.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide as much details as possible"
        }
	]
}
---
