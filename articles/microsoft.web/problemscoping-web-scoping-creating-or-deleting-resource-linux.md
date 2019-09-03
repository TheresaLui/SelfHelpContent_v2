<properties
	pageTitle="Scoping questions for Creating or deleting resources"
	description="Creating or deleting resources"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32542209"
	productPesIds="16170"
	cloudEnvironments="public, MoonCake"
   schemaVersion="1"
   articleId="d5830015-9922-4fff-a95e-fe5f07dbe222"
/>

# Creating or deleting resource
---
{
     "resourceRequired": false,
    "subscriptionRequired": true,
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        },
                {
			"id": "3",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Have you ever been able to create or delete this type of resource before?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
			"required": false
		},
        {
			"id": "4",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Did you try using the InPrivate or Incognito mode of your browser?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
			"required": false
		},
        {
			"id": "5",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "Did you try a different browser (Edge / IE / Chrome)?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
			"required": false
		}
    ],
    "$schema": "SelfHelpContent"
}
---