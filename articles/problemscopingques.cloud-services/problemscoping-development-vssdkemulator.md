<properties
                pageTitle="Development"
                description="Development"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32422596"
                productPesIds="13185"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0118"
	ownershipId="Compute_CloudServices_Content"
/>
# Availability
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Visual Studio, SDK, and emulators",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "if_signin",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Are you able to sign in to Visual Studio with your Azure account?",
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
            "id": "if_removereadd",
            "order": 2,
            "visibility": "if_signin == No",
            "controlType": "dropdown",
            "displayLabel": "Have you tried to remove and re-add the Azure account from Visual Studio?",
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
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
