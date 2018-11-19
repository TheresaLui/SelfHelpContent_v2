<properties
	pageTitle="Storage File Share mounting issues - macOS"
	description="Storage File Share mounting issues - macOS"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602764"
	productPesIds="16460"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Storage File Share mounting issues - macOS
---
{
    "resourceRequired": false,
    "title": "Storage File Share mounting issues - macOS",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "os_version",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "MacOS version where File Share is being mounted",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "OSX_above1011",
                    "text": "El Capitan (version 10.11) or above"
                },
                {
                    "value": "OSX_below1010",
                    "text": "Yosemite (version 10.10) or below"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ]
}
---