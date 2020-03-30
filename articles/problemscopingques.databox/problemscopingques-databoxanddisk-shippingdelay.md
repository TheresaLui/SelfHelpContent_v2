<properties
	articleId="326392005"
	pageTitle="Scoping Questions for shipping delay"
	description="Scoping Questions for shipping delay"
	authors="madhurinms"
	ms.author="madhn"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32639210"
	productPesIds="16505"
	cloudEnvironments="public, Fairfax"
	schemaVersion="1"
    ownershipId="StorageMediaEdge_DataBox"
/>
# Data Box Disk slow copy speed
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Data Box/Disk shipping delay",
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
            "displayLabel": "Select shipping issue",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Carrier tracking says delivered but portal does not reflect the same",
                    "text": "Carrier tracking says delivered but portal does not reflect the sames"
                },
                {
                    "value": "Carrier has not arrived for pick up",
                    "text": "Carrier has not arrived for pick up"
                },
                {
                    "value": "Carrier tracking says delivered but I have not received the package",
                    "text": "Carrier tracking says delivered but I have not received the package"
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
            "visibility": "is_carrier issue == Carrier has not arrived for pick up || Carrier tracking says delivered but I have not received the package",
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
            "id": "previous_solution",
            "visibility": "is_fee_requested == Yes",
            "order": 120,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Additional details about the issue",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
