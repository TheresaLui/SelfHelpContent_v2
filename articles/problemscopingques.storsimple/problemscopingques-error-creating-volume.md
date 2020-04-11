<properties
	articleId="bac4fd19-7d13-4c39-b7ea-088b4e32cea1"
	pageTitle="Scoping error creating new volume"
	description="Error creating new volume or volume container"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630500"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Unable to create new volume or volume container
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Unable to create volume",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "operation_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which operation is failing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Volume creation",
                    "text": "Volume creation"
                },
                {
                    "value": "Volume container creation",
                    "text": "Volume container creation"
                }
            ],
            "required": false
        },
        {
            "id": "volume_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of volume is being created?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Tired volume",
                    "text": "Tired volume"
                },
                {
                    "value": "Locally pinned volume",
                    "text": "Locally pinned volume"
                }
            ],
            "required": false
        },
        {
            "id": "vol_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Provide the name of the volume or volume container for tracking creation calls in the logs?",
            "watermarkTest": "Names of volume or volume container",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
