<properties
	pageTitle="Manage App Registration "
	description="Scoping questions to capture more details about issues encountered while manage App Registration "
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688651"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="D12FEDBF-0A8B-4766-9733-7DE4D88A38B4"
	ownershipId="Compute_BotService"
/>
# Manage App Registration 
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Manage App Registration ",
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
			"id": "operation",
			"order": 3,
			"controlType": "radioButtonGroup",
			"displayLabel": "Are you creating a new app registration or trying to update an existing app registration?",
			"radioButtonOptions": [{
					"value": "new",
					"text": "New app"
				}, {
					"value": "existing",
					"text": "Existing app"
				}
			],
			"required": true
		},
		{
			"id": "mode",
			"order": 4,
			"controlType": "radioButtonGroup",
			"displayLabel": "Was/is the App ID being created automatically or manually? ",
			"radioButtonOptions": [{
					"value": "auto",
					"text": "Automatically"
				}, {
					"value": "manual",
					"text": "Manually"
				}
			],
			"required": true
		},
		{
			"id": "tenant",
			"order": 5,
			"controlType": "radioButtonGroup",
			"displayLabel": "Is the user who created (or is creating) belong to same Azure tenant",
			"radioButtonOptions": [{
					"value": "yes_5",
					"text": "Yes"
				}, {
					"value": "no_5",
					"text": "No"
				}
			],
			"required": true
		},
		{
            "id": "signinaudience",
            "order": 7,
            "controlType": "multiselectdropdown",
            "displayLabel": "Please select the value set in signInAudience attribute in the AAD App manifest?",
			"watermarkText": "To know more about AAD App manifest visit the link in the info balloon.",
			"infoBalloonText": "<a href='https://docs.microsoft.com/azure/active-directory/develop/reference-app-manifest'>Azure Active Directory app manifest</a>",
			"dropdownOptions": [
                {
                    "value": "1",
                    "text": "AzureADMyOrg"
                },
                {
                    "value": "2",
                    "text": "AzureADMultipleOrgs"
                },
                {
                    "value": "3",
                    "text": "AzureADandPersonalMicrosoftAccount"
                },
				{
                    "value": "4",
                    "text": "PersonalMicrosoftAccount"
                }
			]
        },
	{
			"id": "localhost",
			"order": 6,
			"controlType": "radioButtonGroup",
			"displayLabel": "Does the bot work on localhost if you disable App ID and password?",
			"radioButtonOptions": [{
					"value": "yes_6",
					"text": "Yes"
				}, {
					"value": "no_6",
					"text": "No"
				}
			],
			"required": false
		},
		{
			"id": "postman",
			"order": 8,
			"controlType": "radioButtonGroup",
			"displayLabel": "If you are facing an authentication issue, have you tried acquiring a token via Postman or cURL",
			"radioButtonOptions": [{
					"value": "yes_8",
					"text": "Yes"
				}, {
					"value": "no_8",
					"text": "No"
				}
			],
			"watermarkText": "To know more about using Postman/cURL visit the link in the info balloon.",
			"infoBalloonText": "<a href='https://docs.microsoft.com/azure/bot-service/bot-service-troubleshoot-authentication-problems?view=azure-bot-service-4.0#issue-an-http-request-to-the-microsoft-login-service'>Troubleshooting Bot Framework authentication</a>"
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
