<properties
	articleId="problemscopingques-creating-functions-from-source-control"
	pageTitle="Creating functions from source control"
	description="Creating functions from source control"
	supportTopicIds="32518055"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Creating functions from source control
---
{
    "resourceRequired": false,
    "title": "Creating functions from source control",
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
            "id": "4",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Which source repository are you / have you configured for continuous integration?",
            "watermarkText": "...",
            "required": false
        },
        {
            "id": "5",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Are you deploying to a deployment slot or directly into production?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Deployment slot",
                    "text": "Deployment slot"
                },
                {
                    "value": "Production",
                    "text": "Production"
                }
            ],
            "required": false
        },
        {
            "id": "6",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Have you implemented 'run from package'?",
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
            "id": "problem_description",
            "order": 7,
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
