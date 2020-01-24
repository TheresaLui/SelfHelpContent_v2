<properties
    pageTitle="Bandwidth or latency issues"
    description="Bandwidth or latency issues"
    authors="anavinahar"
    ms.author="anavin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32547224"
    productPesIds="15526"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="7ytdr800961cc-d014-45db-be70-2069dc2e00ff"
/>

# Bandwidth or latency issues

---
{
    "resourceRequired": true,
    "title": "Bandwidth or latency issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "from_vm",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the Virtual Machine you are experiencing issues with",
            "watermarkText": "Choose a Virtual Machine",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Network/virtualNetworks/{resourcename}/virtualMachines/$ref?api-version=2017-09-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of Virtual Machines",
                    "text": "Unable to get the list of Virtual Machines"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the IP address",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
