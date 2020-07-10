<properties
	articleId="61c3a139-cfbb-478d-8798-44e59d2ab0cc"
	pageTitle="Scoping for disk drive failure"
	description="Disk drive failure scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630499"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Disk drive failure
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Slow virtual machine",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "disk_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the type for the failed disk",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "HDD",
                    "text": "HDD"
                },
                {
                    "value": "SSD",
                    "text": "SSD"
                }
            ],
            "required": false
        },
        {
            "id": "slot_number",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the slot that holds the failed disk",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Slot 0",
                    "text": "Slot 0"
                },
                {
                    "value": "Slot 1",
                    "text": "Slot 1"
                },
                {
                    "value": "Slot 2",
                    "text": "Slot 2"
                },
                {
                    "value": "Slot 3",
                    "text": "Slot 3"
                },
                {
                    "value": "Slot 4",
                    "text": "Slot 4"
                },
                {
                    "value": "Slot 5",
                    "text": "Slot 5"
                },
                {
                    "value": "Slot 6",
                    "text": "Slot 6"
                },
                {
                    "value": "Slot 7",
                    "text": "Slot 7"
                },
                {
                    "value": "Slot 8",
                    "text": "Slot 8"
                },
                {
                    "value": "Slot 9",
                    "text": "Slot 9"
                },
                {
                    "value": "Slot 10",
                    "text": "Slot 10"
                },
                {
                    "value": "Slot 11",
                    "text": "Slot 11"
                }
            ],
            "required": false
        },
        {
            "id": "unit_type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the unit that holds the failed disk",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Head Unit",
                    "text": "Head Unit"
                },
                {
                    "value": "EBOD",
                    "text": "EBOD"
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
