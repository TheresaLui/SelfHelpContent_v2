<properties
	pageTitle="Cannot connect to other VM in same VNET"
	description="Cannot connect to other VM in same VNET"
	authors="ritup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32584252"
	productPesIds="15526"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="855c0eee-0800-4b92-a5bf-fff3858ca56a"
	ownershipId="CloudNet_VirtualNetwork"
/>
# Cannot connect to another virtual machine in the same VNET
---
{
    "resourceRequired": true,
    "title": "Cannot connect to another virtual machine in the same VNET",
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
            "id": "to_vm",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Please select the VM you are connecting to",
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
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide these details",
            "required": false,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Are you able to connect or ping another VM/Resource on the Internet?"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
