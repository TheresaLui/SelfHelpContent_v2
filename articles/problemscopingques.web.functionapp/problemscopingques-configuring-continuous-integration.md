<properties
	articleId="problemscopingques-configuring-continuous-integration"
	pageTitle="Configuring continuous integration (CI)"
	description="Configuring continuous integration (CI)"
	supportTopicIds="32518048"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Configuring continuous integration (CI)
---
{
    "resourceRequired": false,
    "title": "Configuring continuous integration (CI)",
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
            "displayLabel": "Have you implemented RUN FROM PACKAGE?",
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
