<properties
	articleId="326392006"
	pageTitle="Scoping Questions for Data Box/Disk copy errors"
	description="Scoping Questions for Data Box/Disk copy errors"
	authors="madhurinms"
	ms.author="madhn"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32639201"
	productPesIds="16505"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    ownershipId="StorageMediaEdge_DataBox"
/>
# Data Box Disk slow copy speed
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Data Box Disk slow copy speed",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        },
        {
            "id": "is_copy_error",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Did you run 'Prepare to ship' for Data Box or 'Validation.cmd' for Data Box Disk before shipping?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
