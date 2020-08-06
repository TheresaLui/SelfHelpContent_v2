<properties
                pageTitle="Management"
                description="Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615274"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0094"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Unable to share Shared Image Gallery, Image Definition or Image Version",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "manage_share",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What are you trying to share?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Shared Image Gallery",
                    "text": "Shared Image Gallery"
                },
                {
                    "value": "Image Definition",
                    "text": "Image Definition"
                },
                {
                    "value": "Image Version",
                    "text": "Image Version"
                }
            ],
            "required": false
        },
        {
            "id": "resource_name",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the name of the resource (e.g. image version, gallery1/image1/1.0.0)",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
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
