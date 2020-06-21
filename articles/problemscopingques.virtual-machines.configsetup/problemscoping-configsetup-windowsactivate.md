<properties
                pageTitle="Configuration and Setup"
                description="Configuration and Setup"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32570109"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0084"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Config and Setup
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Issues that are related to activating a Windows license in Azure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "internet_method",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Do you use a VPN, ExpressRoute, or other tunneling method to the Internet?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "VPN",
                    "text": "VPN"
                },
                {
                    "value": "ExpressRoute",
                    "text": "ExpressRoute"
                },
                {
                    "value": "Other tunneling method",
                    "text": "Other tunneling method"
                }
            ],
            "required": false
        },
        {
            "id": "public_IP",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is your public facing IP address?",
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
