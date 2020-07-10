<properties
	articleId="problemscopingques-creating-functions-from-scratch"
	pageTitle="Creating functions from scratch"
	description="Creating functions from scratch"
	supportTopicIds="32518054"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Creating functions from scratch
---
{
    "resourceRequired": false,
    "title": "Creating functions from scratch",
    "fileAttachmentHint": "Please attach any relevant logs/screenshots",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Incident time",
            "required": true
        },
        {
            "id": "3",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "If developing locally, have you upgraded to the most current version of the IDE?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "2",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which IDE are you using?  For example, Visual Studio, Visual Studio Code or in the portal?",
            "watermarkText": "...",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
