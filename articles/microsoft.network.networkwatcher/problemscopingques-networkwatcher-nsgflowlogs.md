<properties
	pageTitle="Issues with NSG Flow Logs"
	description="Issues with NSG Flow Logs"
	authors="damendo"
  ms.author="damendo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32606424"
	productPesIds="16160"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="23f8d822-ea47-49a0-8638-95e9d8d1113f-psq"
	ownershipId="CloudNet_NetAnalytics"
/>

# Issues with NSG Flow Logs
---
{
    "$schema": "SelfHelpContent",
		"subscriptionRequired": true,
		"resourceRequired": false,
    "title": "Issues with NSG Flow Logs",
    "formElements": [
			{
			"id": "problem_start_time",
					"order": 1,
					"controlType": "datetimepicker",
					"displayLabel": "When did the problem start?",
					"required": true
			},
			{
            "id": "nsgq1",
            "visibility": "true",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select your problem type",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                    "value": "config_setup_issue",
                    "text": "Could not enable NSG Flow Logs"
                },{
                    "value": "data_missing",
                    "text": "Not seeing flow log data in storage"
                },{
                    "value": "dont_know_answer",
                    "text": "Other issue"
                }
								],
            "required": true
        },
				{
            "id": "nsgq2",
            "order": 3,
						"visibility": "nsgq1 == config_setup_issue",
            "controlType": "multilinetextbox",
            "displayLabel": "Please paste entire error received when enabling flow logs",
            "required": true
        },
				{
						"id": "nsgq3",
						"order": 4,
						"visibility": "nsgq1 == data_missing",
						"controlType": "multilinetextbox",
						"displayLabel": "Please provide NSG(s) affected, Storage account id, and any recent changes made",
						"required": true
				},
				{
						"id": "problem_description",
						"order": 1000,
						"controlType": "multilinetextbox",
						"displayLabel": "Issue description.",
						"required": true,
						"useAsAdditionalDetails": true,
						"hints": [{
						"text": "Please provide any other details that could be useful."
											}
						]
				}

    ]
}
---
