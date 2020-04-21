<properties
                pageTitle="Configuration and Management"
                description="Configuration and Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32553311"
                productPesIds="13185"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0099"
	ownershipId="Compute_CloudServices_Content"
/>
# Config and Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Certificate management",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "certificate_kind",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which kind of certificates you are referring to?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Service certificates(used for SSL)",
                    "text": "Service certificates(used for SSL)"
                },
                {
                    "value": "Management certificates(used for deployment)",
                    "text": "Management certificates(used for deployment)"
                }
            ],
            "required": false
        },
        {
            "id": "scaling_error",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "cert_resource_info",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide all the information regarding the certificate and the resource.",
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
