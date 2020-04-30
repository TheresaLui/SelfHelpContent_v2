<properties
                pageTitle="Deployment"
                description="Deployment"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32565474,32565476,32565478,32565479,32591243"
                productPesIds="13185"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0101"
	ownershipId="Compute_CloudServices_Content"
/>
# Deployment
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "failure_frequency",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What is the frequency of deployment failure?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Every deployment",
                    "text": "Every deployment"
                },
                {
                    "value": "Fails on multiple retries",
                    "text": "Fails on multiple retries"
                },
                {
                    "value": "Intermittent",
                    "text": "Intermittent"
                }
            ],
            "required": false
        },
        {
            "id": "if_fromportal",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Does this issue occur when deploying from the portal?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "Have not tried it",
                    "text": "Have not tried it"
                },
                {
                    "value": "Happens only from client tools (VS, PS)",
                    "text": "Happens only from client tools (VS, PS)"
                }
            ],
            "required": false
        },
        {
            "id": "deploy_error",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the exact error message (include Operation ID etc).",
            "required": false,
            "useAsAdditionalDetails": false
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
