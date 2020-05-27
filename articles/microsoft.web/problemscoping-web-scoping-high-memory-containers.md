<properties
	pageTitle="Scoping questions for high memory usage"
	description="High memory usage"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32581616"
	productPesIds="16333"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="ccbd-4b55-8191-4539de3408c8"
	ownershipId="Compute_AppService"
/>

# High memory usage
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
			"displayLabel": "Has the site volume increased?",
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
			"controlType": "textbox",
			"displayLabel": "Which indicators are you looking at for memory usage?",
			"watermarkText": "...",
			"required": false
		},
        {
			"id": "5",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "How much memory consumption are you seeing?",
			"watermarkText": "...",
			"required": false
		},
        {
			"id": "6",
			"order": 6,
			"controlType": "textbox",
			"displayLabel": "Is the issue still occurring? If not, how was the issue resolved?",
			"watermarkText": "...",
			"required": false
		}],
    "$schema": "SelfHelpContent"
}
---
