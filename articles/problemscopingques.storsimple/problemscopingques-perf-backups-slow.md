<properties
	articleId="d3b082b9-d862-4d13-b8e8-78a8a49b909f"
	pageTitle="Scoping for Backups slow"
	description="Backups slow scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630494"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Backups are slow
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Backups_slow",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "local_backups",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Are the local backup successful?",
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
            "id": "cloud_bandwidth",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Specify the cloud bandwidth available to StorSimple",
            "watermarkText": "Cloud bandwidth in Mbps",
            "required": false
        },
        {
            "id": "dedicated_or_shared",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the cloud bandwidth dedicated or shared?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Dedicated",
                    "text": "Dedicated"
                },
                {
                    "value": "Shared",
                    "text": "Shared"
                }
            ],
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
