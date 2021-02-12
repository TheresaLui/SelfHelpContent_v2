<properties
	pageTitle="Billing"
	description="Scoping questions to capture more details about billing"
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688618"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="{D38D5B24-C104-49C7-804F-9A801C61EEDC}"
	ownershipId="Compute_BotService"
/>
# Billing
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Billing",
    "fileAttachmentHint": "Please upload screenshots that will help us understand the issue",
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
			"id": "error_advice",
			"order": 3,
			"controlType": "radioButtonGroup",
			"displayLabel": "Which of the following you need help with?",
			"radioButtonOptions": [
			    {
					"value": "pricing",
					"text": "Advice on pricing or charges"
				},
				{
					"value": "incorrect",
					"text": "Incorrect billing"
				},
				{
					"value": "monitor",
					"text": "How to monitor or view usage or billing"
				},
				{
					"value": "plan",
					"text": "Change bot service plan"
				},
				{
					"value": "Other",
					"text": "Need help with something else"
				}
			],
			"required": true
		},
		{
			"id": "b1",
			"order": 4,
			"visibility":"error_advice == incorrect",
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide the billing cycle, time period details of when you believe you are incorrectly charged",
			"required": true
		},
		{
			"id": "b2",
			"order": 5,
			"visibility":"error_advice == monitor",
			"controlType": "multilinetextbox",
			"displayLabel": "If you are facing any issues in viewing the bot costs or charges, please provide the details and error message",
			"required": true,
			"watermarkText": "Upload a screenshot of the error via the file upload option below. Also provide details on your role in the Subscription. Some accounts or roles may not have the necessary permissions to view  billing details, contact your Subscription account admin to get the necessary permissions."
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
