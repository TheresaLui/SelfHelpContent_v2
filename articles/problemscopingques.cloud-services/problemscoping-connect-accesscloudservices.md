<properties
                pageTitle="Connectivity"
                description="Connectivity"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32565482"
                productPesIds="13185"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0119"
	ownershipId="Compute_CloudServices_Content"
/>
# Connectivity
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Problem that is related to accessing Cloud Services",
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
            "id": "error_message",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message do you receive when you try to connect to the resource from Cloud Service?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "network_trace",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Did you collect any network traces during connectivity issue? If yes, please upload them and share the client IP address.",
            "useAsAdditionalDetails": false,
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
