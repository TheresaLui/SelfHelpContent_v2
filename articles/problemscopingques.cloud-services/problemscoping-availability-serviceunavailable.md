<properties
                pageTitle="Application and Service Availability"
                description="Application and Service Availability"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32591241"
                productPesIds="13185"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0098"
	ownershipId="Compute_CloudServices_Content"
/>
# Availability
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Service was or is unavailable",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "connect_url",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Can you connect to {cloudserviceName}.cloudapp.net URL?",
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
            "id": "unavailable_symptoms",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What were the exact symptoms during the time the service was unavailable?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "if_collectdata",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Have you collected any data during the time of the issue? If yes, please share.",
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
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
