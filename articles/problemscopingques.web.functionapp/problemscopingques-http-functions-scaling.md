<properties
	articleId="problemscopingques-http-functions-scaling"
	pageTitle="HTTP Functions Scaling"
	description="HTTP Functions Scaling"
	supportTopicIds="32630475"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# HTTP Functions Scaling
---
{
    "resourceRequired": false,
    "title": "HTTP Functions Scaling",
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
            "controlType": "dropdown",
            "displayLabel": "How would you describe your HTTP Traffic pattern? Would it be a consistent load or a burst of HTTP traffic intermittently?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Consistent load ",
                    "text": "Consistent load "
                },
                {
                    "value": "Burst",
                    "text": "Burst"
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
