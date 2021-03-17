<properties
                pageTitle="Planned Maintenance (Azure Platform)"
                description="Planned Maintenance (Azure Platform)"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supporttopicids="32783376,32783377,32783378,32783379"
                productPesIds="16080"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="c0e530a1-b3bd-4cff-b9ff-3bdece0fd14d"
                ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# Planned Maintenance (Azure Platform)
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Planned Maintenance (Azure Platform)",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "maintenance_notification",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Did you receive a maintenance notification for your resource?",
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
            "id": "tracking_id",
            "order": 2,
            "visibility": "maintenance_notification == Yes",
            "controlType": "textbox",
            "displayLabel": "What is the tracking ID of the notification that you received?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "maintenance_selfservice",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Did you attempt to perform self-service maintenance based on Service Health information?",
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
            "id": "selfservice_result",
            "order": 4,
            "visibility": "maintenance_selfservice == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Please enter the result.",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
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
