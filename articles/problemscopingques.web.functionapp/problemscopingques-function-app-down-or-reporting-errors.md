<properties
	articleId="problemscopingques-function-app-down-or-reporting-errors"
	pageTitle="Function App down or reporting errors"
	description="Function App down or reporting errors"
	supportTopicIds="32630466"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Function App down or reporting errors
---
{
    "resourceRequired": false,
    "title": "Function App down or reporting errors",
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
            "displayLabel": "Is the Function processing partially or does it time out",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Partially",
                    "text": "Partially"
                },
                {
                    "value": "Time out",
                    "text": "Time out"
                }
            ],
            "required": false
        },
        {
            "id": "7",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "If possible, please provide an Invocation Id of a Function execution which was slow.  The Invocation Id resembles a GUID and can be found in the Invocation Detail log on the Monitor blade in the portal.  It is most commonly the final entry.",
            "watermarkText": "...",
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
