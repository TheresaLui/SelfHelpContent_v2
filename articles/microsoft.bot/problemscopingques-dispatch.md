<properties
	pageTitle="Dispatch or Routing"
	description="Scoping questions to capture more details about Dispatch or Routing "
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688640"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="C47FF9ED-A392-49D0-AEA1-18F12848F26C"
	ownershipId="Compute_BotService"
/>
# Dispatch or Routing 
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Dispatch or Routing ",
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
			"id": "mode",
			"order": 3,
			"controlType": "radioButtonGroup",
			"displayLabel": "What version of the Bot Framework SDK are you using? ",
			"radioButtonOptions": [{
					"value": "3",
					"text": "Version 3"
				}, {
					"value": "3b",
					"text": "Version 4"
				}
			],
			"infoBalloonText": "Check the version of Microsoft.Bot.Builder version used by your bot application. If it is 4.x.x, it is using SDK v4, and if it is 3.x.x, it is using SDK v3",
			"required": true
		},
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details, if you see an error message list it or you are looking for specific guidance. Provide steps to repro as well.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide as much details as possible"
        }
	]
}
---
