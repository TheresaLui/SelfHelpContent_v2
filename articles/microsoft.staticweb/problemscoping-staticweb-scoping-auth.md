<properties
	pageTitle="Scoping questions for Static Web App Auth"
	description="Auth"
	service="microsoft.staticweb"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32741853"
	productPesIds="17265"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="22873c27-8f6c-4cee-82df-e50ea942dc600"
	ownershipId="Compute_AppService"
/>

# Auth
---
{
	"resourceRequired": false,
	"fileAttachmentHint": "GitHub action logs",
	"formElements": [{
		"id": "q1",
		"order": 1,
		"controlType": "dropdown",
		"displayLabel": "How is the static front end for your application implemented?",
		"watermarkText": "Choose an option",
		"dropdownOptions": [{
				"value": "JavaScript",
				"text": "JavaScript"
			},
			{
				"value": "Vue.jsr",
				"text": "Vue.js"
			},
			{
				"value": "React",
				"text": "React"
			},
			{
				"value": "Angular",
				"text": "Angular"
			},
			{
				"value": "Static site generator",
				"text": "Static site generator"
			},
			{
				"value": "Other",
				"text": "Other"
			}
		],
		"required": false
	}, {
		"id": "problem_start_time",
		"order": 2,
		"controlType": "datetimepicker",
		"displayLabel": "Problem start time",
		"required": true
	}, {
		"id": "q3",
		"order": 3,
		"controlType": "multilinetextbox",
		"displayLabel": "Description",
		"watermarkText": "Is there a specific error you are observing with your application?",
		"required": false
	}],
	"$schema": "SelfHelpContent"
}
---
