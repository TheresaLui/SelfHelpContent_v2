<properties
	articleId="problemscopingques-app-servic-built-in-authentication-through-portal"
	pageTitle="App Service Built-in Authentication through Portal"
	description="App Service Built-in Authentication through Portal"
	supportTopicIds="32607515"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# App Service Built-in Authentication through Portal
---
{
    "resourceRequired": false,
    "title": "App Service Built-in Authentication through Portal",
    "subscriptionRequired": true,
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
            "displayLabel": "Did you use the Express or Advanced settings to configure the authentication provider?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Express",
                    "text": "Express"
                },
                {
                    "value": "Advanced",
                    "text": "Advanced"
                }
            ],
            "required": false
        },
        {
            "id": "3",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Which Authentication provider are you using?",
            "watermarkText": "Authentication provider...",
            "required": false
        },
        {
            "id": "4",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What exception are you experiencing?",
            "watermarkText": "Exception...",
            "required": false
        },
        {
            "id": "5",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Have you implemented any Gateways or are there other devices which you are ware of which might interfere with authentication? If yes please explain in th additional details",
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
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your incident including any error messages you are seeing.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
