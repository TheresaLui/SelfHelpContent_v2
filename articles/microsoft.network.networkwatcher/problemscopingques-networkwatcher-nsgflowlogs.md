<properties
	pageTitle="Issues with NSG Flow Logs"
	description="Issues with NSG Flow Logs"
	authors="damendo"
  ms.author="damendo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32606424"
	productPesIds="16160"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="23f8d822-ea47-49a0-8638-95e9d8d1113f"
/>

# Issues with NSG Flow Logs
---
{
    "$schema": "SelfHelpContent",
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
                    "value": "Configuration/Setup issue",
                    "text": "Could not enable NSG Flow Logs"
                },{
                    "value": "Data missing",
                    "text": "Not seeing flow log data in storage"
                },{
                    "value": "Other issue",
                    "text": "Other issue"
                }
								],
            "required": true
        },
				{
            "id": "nsgq2",
            "order": 3,
						"visibility": "nsgq1 == Configuration/Setup issue",
            "controlType": "multilinetextbox",
            "displayLabel": "Issue description",
            "required": true,
            "useAsAdditionalDetails": true,
						"hints": [{
            "text": "Please paste entire error received when enabling flow logs"
        							},
    				]
        },
				{
						"id": "nsgq3",
						"order": 4,
						"visibility": "nsgq1 == Data missing",
						"controlType": "multilinetextbox",
						"displayLabel": "Issue description",
						"required": true,
						"useAsAdditionalDetails": true,
						"hints": [{
            "text": "Please provide NSG(s) affected, Storage account id, and recent changes made if any."
        							},
    				]

				},
				{
						"id": "problem_description",
						"order": 1000,
						"visibility": "nsgq1 == Other issue",
						"controlType": "multilinetextbox",
						"displayLabel": "Issue description.",
						"required": false,
						"useAsAdditionalDetails": true,
						"hints": [{
						"text": "Please provide details more details like NSGs, subnets, etc. to enable faster resolution."
											},
						]
				}

    ]
}
