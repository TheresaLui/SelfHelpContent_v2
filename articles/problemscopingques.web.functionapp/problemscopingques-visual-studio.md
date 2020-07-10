<properties
	articleId="problemscopingques-visual-studio"
	pageTitle="Visual Studio"
	description="Visual Studio"
	supportTopicIds="32630472"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Visual Studio
---
{
    "resourceRequired": false,
    "title": "Visual Studio",
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
            "id": "2",
            "order": 2,
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
            "id": "3",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What deployment exception are you experiencing?",
            "watermarkText": "...",
            "required": false
        },
        {
            "id": "4",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What version of Visual Studio are you deploying from?  Please confirm you have the most current updates for that version",
            "watermarkText": "...",
            "required": false
        },
        {
            "id": "5",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Have you tried deploying from another location outside of any corporate network restrictions?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "NA",
                    "text": "NA"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
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
