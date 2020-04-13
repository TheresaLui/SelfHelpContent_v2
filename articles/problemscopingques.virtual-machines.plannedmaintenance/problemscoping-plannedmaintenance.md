<properties
                pageTitle="Planned Maintenance (Azure Platform)"
                description="Planned Maintenance (Azure Platform)"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32589415,32641081"
                productPesIds="14749,15571,15797,16454,16470,16080"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0066"
	ownershipId="Compute_VirtualMachines_Content"
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
