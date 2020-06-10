<properties
	pageTitle="Azure RTOS Filex Issues"
	description="Azure RTOS Scoping Questions to capture more information"
	authors="michamay"
	ms.author="micmay"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32725740"
	productPesIds="16920"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="085670ec-9648-472b-abd4-da8fc20372fe"
	ownershipId="Azure_RTOS"
/>
# Problem Description
---
{
	"$schema": "SelfHelpContent",
	"subscriptionRequired": false,
	"resourceRequired": false,
	"title": "What version are you using",
	"fileAttachmentHint": "",
	"formElements": [{
		"id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
       }, {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false
        }, {
		"id": "problem_description",
		"order": 3,
		"controlType": "multilinetextbox",
		"displayLabel": "Please provide a description of the problem including;",
		"watermarkText": "provide as much of the above information here as you can",
		"required": true,
		"useAsAdditionalDetails": true,
		"hints": [{
			"text": "A list of the events that manifested the problem."
		}, {
			"text": "Any recent code changes or updates that might have triggered the issue."
		}, {
			"text": "The contents of the 'build_option' variable."
		}, {
			"text": "A sample program that exhibits the problem, if possible."
		}]
	}, {
		"id": "User Guides",
		"order": 4,
		"controlType": "infoblock",
		"content": "<a href='https://docs.microsoft.com/azure/rtos/'>please refer to the User Guide</a> for more information"
	}]
}
---
