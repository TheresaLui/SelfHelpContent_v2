<properties
                pageTitle="Cannot Start or Stop My Virtual Machine"
                description="Cannot Start or Stop My Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628260"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0011"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Start or Stop My VM
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "I am unable to resize my VM",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "startstop_size",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the size of the VM you are trying to deploy?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "startstop_isinscaleset",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you deploying your VM in a scale set?",
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
            "id": "startstop_inportal",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Did you have problem resizing in portal?",
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
            "useAsAdditionalDetails": false,
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
