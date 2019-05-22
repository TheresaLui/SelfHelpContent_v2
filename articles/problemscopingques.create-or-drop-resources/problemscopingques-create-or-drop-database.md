<properties
	pageTitle="Create or Drop a Database"
	description="Create or Drop a Database"
	authors="Johirsch"
	ms.author="Johirsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630418"
	productPesIds="13491"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-createordropdatabase"
/>

# Create or Drop a Database
---
{
	"resourceRequired": true,
	"title": "Database",
	"fileAttachmentHint": "",
	"resourceRequired": true,
	"subscriptionRequired": true,
	"formElements": [
		{
			"id": "which_operation",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Which operation are you having trouble with?",
			"watermarkText": "Select one",
			"infoBalloonText": "Which of these is causing issues?",
			"dropdownOptions": [{
					"value": "dont_know_answer",
					"text": "Other"
			}],
			"dynamicDropdownOptions": {
				"uri": "{resourceId}/operations?api-version=2017-10-01-preview",
				"jtokenPath": "value",
				"textProperty": "name",
				"valueProperty": "id",
				"textPropertyRegex": null
			},
			"required": false,
			"useAsAdditionalDetails": false,
			"visibility": true
		},
      		{
			"id": "problem_description",
			"order": 2,
			"controltype": "multilinetextbox",
			"displayLabel": "Any additional details you would like to include?",
			"watermarkText": "Enter any additional details here",
			"infoBalloonText": "Enter any additional details here",
			"required": true,
			"useAsAdditionalDetails": true
		},
		{
			"id": "problem_start_time",
			"order": 3,
			"controltype": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"watermarkText": "Specify when the problem started",
			"infoBalloonText": "Specify when the problem started",
			"required": true,
			"useAsAdditionalDetails": false
		}
	]
}
---
