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
	"resourceRequired": true,
	"subscriptionRequired": true,
	"formElements": [
	        {
		        "id": "which_operation",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Which of these operations is causing trouble?",
			"watermarkText": "Choose an option",
			"infoBalloonText": "Which of these current scaling operations is problematic?",
			"dynamicDropdownOptions": {
            			"uri": "{resourceId}/operations?api-version=2017-10-01-preview",
            			"jTokenPath": "value",
            			"textProperty": "id",
            			"valueProperty": "id",
            			"textPropertyRegex": null
        		},
			"required": false,
			"useAsAdditionalDetails": false,
			"visibility": true
	        },
	        {
			"id": "ongoing_or_completed_updateslo",
			"order": 2,
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
			"required": false,
			"useAsAdditionalDetails": false,
			"visibility": true
		},
		{
			"id": "db_or_epool",
			"order": 3,
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
			"required": false,
			"useAsAdditionalDetails": false,
			"visibility": true
		},
		{
			"id": "db_source_tier",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Which service tier are you trying to scale from?",
			"watermarkText": "Choose an option",
			"infoBalloonText": "From which service tier did you initiate the scaling operation?",
			"dropdownOptions": [{
					"value": "db_basic",
					"text": "Basic or Standard(S0-S2)"
				},{
					"value": "db_standard",
					"text": "Standard(S3-S12), General Purpose, or Hyperscale"
				},{
					"value": "db_premium",
					"text": "Premium or Business Critical"
				},{
					"value": "dont_know_answer",
					"text": "Other"
				}
			],
			"required": false,
			"useAsAdditionalDetails": false,
			"visibility": "db_or_epool == Database"
		},
		{
			"id": "db_target_tier",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "Which service tier are you trying to scale to?",
			"watermarkText": "Choose an option",
			"infoBalloonText": "To which service tier are you attempting to scale?",
			"dropdownOptions": [{
					"value": "db_basic",
					"text": "Basic or Standard(S0-S2)"
				},{
					"value": "db_standard",
					"text": "Standard(S3-S12), General Purpose, or Hyperscale"
				},{
					"value": "db_premium",
					"text": "Premium or Business Critical"
				},{
				        "value": "elastic_pool",
					"text": "Elastic Pool"
				},{
					"value": "dont_know_answer",
					"text": "Other"
				}
			],
			"required": false,
			"useAsAdditionalDetails": false,
			"visibility": "db_or_epool == Database"
		},
		{
			"id": "ep_source_tier",
			"order": 6,
			"controlType": "dropdown",
			"displayLabel": "Which service tier are you trying to scale from?",
			"watermarkText": "Choose an option",
			"infoBalloonText": "From which service tier did you initiate the scaling operation?",
			"dropdownOptions": [{
					"value": "ep_basic",
					"text": "Basic"
				},{
					"value": "ep_standard",
					"text": "Standard or General Purpose"
				},{
					"value": "ep_premium",
					"text": "Premium or Business Critical"
				},{
					"value": "dont_know_answer",
					"text": "Other"
				}
			],
			"required": false,
			"useAsAdditionalDetails": false,
			"visibility": "db_or_epool == Elastic_Pool"
		},
		{
			"id": "ep_target_tier",
			"order": 7,
			"controlType": "dropdown",
			"displayLabel": "Which service tier are you trying to scale to?",
			"watermarkText": "Choose an option",
			"infoBalloonText": "To which service tier are you attempting to scale?",
			"dropdownOptions": [{
					"value": "ep_basic",
					"text": "Basic"
				},{
					"value": "ep_standard",
					"text": "Standard or General Purpose"
				},{
					"value": "ep_premium",
					"text": "Premium or Business Critical"
				},{
				        "value": "single_database",
					"text": "Single Database"
				},{
					"value": "dont_know_answer",
					"text": "Other"
				}
			],
			"required": false,
			"useAsAdditionalDetails": false,
			"visibility": "db_or_epool == Elastic_Pool"
		},
		{
			"id": "database_size",
			"order": 8,
			"controlType": "textbox",
			"displayLabel": "How large is your database?",
			"watermarkText": "How large is your database?",
			"infoBalloonText": "What size is your database?",
			"required": false,
			"useAsAdditionalDetails": false,
			"visibility": true
		},
		{
			"id": "problem_description",
			"order": 9,
			"controltype": "multilinetextbox",
			"displayLabel": "Any additional details you would like to include?",
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
