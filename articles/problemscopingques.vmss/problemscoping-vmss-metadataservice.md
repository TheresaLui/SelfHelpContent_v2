<properties
                pageTitle="Management"
                description="Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32591160"
                productPesIds="16080"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0108"
/>
# Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure Metadata Service (Scheduled Events)",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "manage_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "tracking_id",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Share the tracking ID of planned maintenance, for which you configured the scheduled events.",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "primary_issue_category",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What is the primary issue category?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Creating scheduled events",
                    "text": "Creating scheduled events"
                },
                {
                    "value": "Want to learn more about scheduled events",
                    "text": "Want to learn more about scheduled events"
                },
                {
                    "value": "Functionality issues",
                    "text": "Functionality issues"
                }
            ],
            "required": false
        },
        {
            "id": "if_alert",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Did you receive an alert for the VM indicating a planned maintenance event needing a restart?",
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
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
