<properties
	pageTitle="Cannot RDP or SSH to VM"
	description="Cannot RDP or SSH to VM"
	authors="ritup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32547225"
	productPesIds="15526"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="bd533d79-d3fa-439d-964a-2982e28e8ea5"
	ownershipId="CloudNet_VirtualNetwork"
/>
# Cannot connect to virtual machine using RDP or SSH
---
{
    "resourceRequired": true,
    "title": "Cannot connect to virtual machine using RDP or SSH",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "cannot_connect_vm",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the VM you are not able to RDP or SSH to?",
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
            "order": 2,
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
                    "text": "Are you able to tcping the VM's IP address?"
                },
                {
                    "text": "Are you able to RDP/SSH to other VMs in this VNet?"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
