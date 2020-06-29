<properties
	articleId="problemscopingques-peeringservice-configuration"
	pageTitle="Scoping Questions for Peering Service Configuration/Registration"
	description="Scoping Questions for Peering Service Configuration/Registration"
	authors="brianlehr"
    ms.author="blehr"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32689967"
	productPesIds="16932"
	cloudEnvironments="public,mooncake,fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Peering_PeeringService"
/>

# Configuration/Registration Scoping Questions
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Peering Service Configuration",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "locations",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What is your location and where is the Location you are attempting to user for Peering Service?",
            "watermarkText": "Please List Both Locations",
            "required": false
        },
        {
            "id": "distance_warning",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Did you receive a warning that the selected Location for a Peering Service connection is over 500 miles (800 kms) from your location?",
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
            "required": false
        },
        {
            "id": "public_ip",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Did you receive validation error message when attempting to register prefix in a Peering Service connection?  If so, what?",
            "watermarkText": "Please provide error message",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---