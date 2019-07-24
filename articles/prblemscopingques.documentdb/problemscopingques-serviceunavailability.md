<properties
	pageTitle="CosmosDB Service Unavailability Issue"
	description="CosmosDB Service Unavailability Issue"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636827"
	productPesIds="15585"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="c826999a-6b04-4e85-930c-f9a1c14c27e6"
/>
# CosmosDB Service Unavailability Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "CosmosDB Service Unavailability Issue",
    "fileAttachmentHint": "Please attach your stack trace exceptions in a flat text file.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
		{
            "id": "problem_duration",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "How long was the issue observed?",
            "required": false
        },
		{
            "id": "region_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Which region is your client running?",
            "required": false
        },
		{
            "id": "connectivity_mode",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Which connectivity mode is your client using?",
			"infoBalloonText": "This is specified in the connection policy of the constructor for the Document client. Default is gateway",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Gateway",
                    "text": "Gateway"
                },
                {
                    "value": "Direct",
                    "text": "Direct"
                }
            ],
            "required": false
        },
		{
            "id": "database_name",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Database name",
            "required": false
        },
        {
            "id": "collection_name",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Collection name",
            "required": false
        },
		{
            "id": "exception_count",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "How many service unavailable exceptions did you observe?",
            "required": false
        },
		{
            "id": "vm_count",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "Number of VMs the exception was seen during this time.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you were facing",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the exact issue."
                },
                {
                    "text": "Read/Write regions where the issue is experienced"
                },
                {
                    "text": "Activity Id of the request (if available)."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
