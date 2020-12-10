<properties
	pageTitle="Data Share common scoping questions"
	description="Scoping questions to capture more details about errors encountered while using Data Share"
	ms.author="hecepeda"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32675618,32675619,32748890,32748891,32748882,32748883,32748884,32748885,32675621,32675628,32748887,32748888,32748889,32675629"
	productPesIds="16762"
	cloudEnvironments="public,fairfax,usnat,ussec,mooncake,blackforest"
	schemaVersion="1"
	articleId="probemscopingques_datashare_general"
	ownershipId="AzureData_DataShare"
/>
# General Data Share Questions
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Data Share General Questions",
    "fileAttachmentHint": "Please include any screenshots or logs that might help narrowing down the problem",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Always provide the full error text."
        }
    ]
}
---
