<properties
	pageTitle="Issues Scaling a Database or Elastic Pool"
	description="Issues Scaling a Database or Elastic Pool"
	authors="Johirsch"
	ms.author="Johirsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630431"
	productPesIds="13491"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-scalingissues"
/>

# Issues Scaling a Database or Elastic Pool
---
{
	"resourceRequired": true,
	"title": "Issues Scaling a Database or Elastic Pool",
	"fileAttachmentHint": "",
	"formElements": [
	{
			"id": "ongoing_or_completed_updateslo",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Do you need help with an ongoing scaling operation, or one that's already finished?",
			"watermarkText": "Choose an option",
			"infoBalloonText": "Is the scaling operation you need help with still in progress, or has it concluded?",
			"dropdownOptions": [{
					"value": "Ongoing",
					"text": "Ongoing"
				},{
					"value": "Completed/Terminated",
					"text": "Completed/Terminated"
				},{
			                "value": "dont_know_answer",
					"text": "I'm not sure"
				}
			],
			"required": true,
			"useAsAdditionalDetails": false,
			"visibility": true
		},
		{
			"id": "db_or_epool",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Are you trying to scale a database, or an elastic pool?",
			"watermarkText": "Choose an option",
			"infoBalloonText": "Does the scaling operation in question target a database, or an elastic pool?",
			"dropdownOptions": [{
					"value": "Database",
					"text": "Database"
				},{
					"value": "Elastic_Pool",
					"text": "Elastic Pool"
				},{
					"value": "dont_know_answer",
					"text": "I'm not sure"
				}
			],
			"required": true,
			"useAsAdditionalDetails": false,
			"visibility": true
		},
		{
			"id": "db_source_tier",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Which service tier are you trying to scale from?",
			"watermarkText": "Choose an option",
			"infoBalloonText": "From which source tier did you initiate the scaling operation?",
			"dropdownOptions": [{
					"value": "db_basic",
					"text": "Basic or Standard(S0-S2)"
				},{
					"value": "db_standard",
					"text": "Standard(S3-S12), General Purpose, or Hyperscale"
				},{
					"value": "db_premium",
					"text": "Premium or Business Critical"
				}
			],
			"required": true,
			"useAsAdditionalDetails": false,
			"visibility": "db_or_epool == Database"
		},
		{
			"id": "problem_description",
			"order": 9,
			"controltype": "multilinetextbox",
			"displayLabel": "TEST3",
			"watermarkText": "Enter any additional details here",
			"infoBalloonText": "Enter any additional details here",
			"required": true,
			"useAsAdditionalDetails": true
		},
		{
			"id": "problem_start_time",
			"order": 10,
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
