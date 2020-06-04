<properties
	articleId="326392003"
	pageTitle="Scoping Questions for Data Box Disk not detected"
	description="Scoping Questions for Data Box Disk not detected"
	authors="madhurinms"
	ms.author="madhn"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32639208"
	productPesIds="16505"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    ownershipId="StorageMediaEdge_DataBox"
/>
# Cannot unlock or write to Data Box Disk 
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Cannot unlock or write to Data Box Disk",
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
            "id": "is_disk_issue",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What is the error seen?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "There is no file system on the disk",
                    "text": "There is no file system on the disk"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "previous_solution",
            "visibility": "is_disk_issue == There is no file system on the disk || is_disk_issue == dont_know_answer",
            "order": 110,
            "controlType": "dropdown",
            "displayLabel": "Did you format the disk?",
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
            "watermarkText": "Please provide full error text and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
