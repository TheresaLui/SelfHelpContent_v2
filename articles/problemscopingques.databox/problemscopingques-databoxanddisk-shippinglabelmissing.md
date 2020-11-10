<properties
	articleId="326392009"
	pageTitle="Scoping Questions for shipping delay"
	description="Scoping Questions for shipping delay"
	authors="madhurinms"
	ms.author="madhn"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32639205"
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
    "title": "Data Box/Disk shipping label needed",
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
            "id": "is_carrier issue",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select shipping label issue",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I have lost the shipping label and I cannot download it from the portal overview page",
                    "text": "I have lost the shipping label and I cannot download it from the portal overview page"
                },
                {
                    "value": "Am using Data Box, ran into issues during prepare to ship and cannot download a shipping label",
                    "text": "Am using Data Box, ran into issues during prepare to ship and cannot download a shipping label"
                },
                {
                    "value": "Am using Data Box Disk and used the label to send few disks, need label to send the remaining",
                    "text": "Am using Data Box Disk and used the label to send few disks, need label to send the remaining"
                },
                {
                    "value": "Carrier says my shipping label has expired",
                    "text": "Carrier says my shipping label has expired"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "is_fee_requested",
            "visibility": "is_carrier issue == Carrier has not arrived for pick up || is_carrier issue == Carrier tracking says delivered but I have not received the package",
            "order": 110,
            "controlType": "dropdown",
            "displayLabel": "Did you contact the carrier regarding the package status",
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
