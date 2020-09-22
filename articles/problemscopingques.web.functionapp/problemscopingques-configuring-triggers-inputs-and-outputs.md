<properties
	articleId="problemscopingques-configuring-triggers-inputs-and-outputs"
	pageTitle="Configuring triggers, inputs, and outputs"
	description="Configuring triggers, inputs, and outputs"
	supportTopicIds="32518051"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Configuring triggers, inputs, and outputs
---
{
    "resourceRequired": false,
    "title": "Configuring triggers, inputs, and outputs",
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
            "controlType": "textbox",
            "displayLabel": "Please provide the Function name that is not working as expected",
            "watermarkText": "function name...",
            "required": false
        },
        {
            "id": "3",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the function.json file",
            "watermarkText": "function.json...",
            "required": false
        },
        {
            "id": "4",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the host.json file",
            "watermarkText": "host.json...",
            "required": false
        },
        {
            "id": "5",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What exception are you experiencing?",
            "watermarkText": "exception...",
            "required": false
        },
        {
            "id": "6",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Does the reported issue occur from the input or output binding?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "input",
                    "text": "input"
                },
                {
                    "value": "output",
                    "text": "output"
                }
            ],
            "required": false
        },
        {
            "id": "7",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Are you declaratively or imperatively defining your bindings?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "declaratively",
                    "text": "declaratively"
                },
                {
                    "value": "imperatively",
                    "text": "imperatively"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
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
