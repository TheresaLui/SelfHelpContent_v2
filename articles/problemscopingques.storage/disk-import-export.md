<properties
	pageTitle="Scoping Questions for Disk Import/Export"
	description="Scoping Questions for Disk Import/Export"
	authors="ansubram"
	ms.author="anushasubramanian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32603552"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="diskImportExport1"
/>
# Disk Import/Export issues
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Disk Import/Export issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When was the problem first observed?",
            "required": true
        },
        {
            "id": "job_name",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Please select the job name",
            "required": true,
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
           	 "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.ImportExport/jobs?api-version=2016-11-01",
            	"jTokenPath": "value",
            	"textProperty": "name",
            	"valueProperty": "id",
            	"textPropertyRegex": "[^/]+$",
            	"defaultDropdownOptions": {
                	"value": "dont_know_answer",
                	"text": "Other, don't know or not applicable"
            	}
        }
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the details regarding the issue and and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
	],
	"$schema": "SelfHelpContent"
}
---
