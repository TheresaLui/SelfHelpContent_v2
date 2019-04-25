<properties
	articleId="problemscopingques-runas.md"
	pageTitle="Azure Automation - Run As Account"
	description="Azure Automation - Run As Account"
	authors="zjalexander"
	ms.author="zachal"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628004,32628007,32628010,32628011"
	productPesIds="15607"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# RunAs Account
---
{
	"resourceRequired": false,
	"title": "Automation Account",
	"fileAttachmentHint": "Please provide a screenshot of any errors",
    "formElements":
    [
        {
			"id": "problem_start_time",
			"order": 10,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
        },
		{
            "id": "RunasAccountType",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the RunAs account a Classic RunAs?",
            "dropdownOptions": [
                {
                    "value": "ARM",
                    "text": "No, this is an Azure Run As account"
                },
                {
                    "value": "Classic",
                    "text": "Yes, this is a Classic Run As account"
                },
            ],
            "required": false
        },
        {
			"id": "problem_description",
			"order": 30,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available",
			"required": true,
			"useAsAdditionalDetails": true,
            "hints":
            [
                {
					"text": "Include the exact text of any error messages that occur"
				}
			]
		}
	]
}
---
