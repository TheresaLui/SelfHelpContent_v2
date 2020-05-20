<properties
    pageTitle="Cannot connect to other VM on-prem"
    description="Cannot connect to other VM on-prem"
    authors="ritup"
    ms.author="anavin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32584251"
    productPesIds="15526"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="700961cc-d014-45db-be70-2069dc2e00ff"
	ownershipId="CloudNet_VirtualNetwork"
/>

# Cannot connect to another virtual machine on-prem

---
{
    "resourceRequired": true,
    "title": "Cannot connect to another virtual machine on-prem",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "from_vm",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the VM you are connecting from",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Network/virtualNetworks/{resourcename}/virtualMachines/$ref?api-version=2017-09-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of VM's",
                    "text": "Unable to get the list of VM's"
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
            "displayLabel": "Please provide these details",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Please provide the on-prem IP you are connecting to."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
