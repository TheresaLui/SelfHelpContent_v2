<properties
	pageTitle="Cannot Connect to a VM in a peered VNet"
	description="Cannot Connect to a VM in a peered VNet"
	authors="KristinaNeyens"
	selfHelpType="problemScopingQuestions"
	articleid="cannotconnectVMinapeeredVNET"
	supportTopicIds="32584249"
	productPesIds="15526"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_VirtualNetwork"
/>
# Cannot Connect to a VM in a peered VNet
---
{
    "resourceRequired": true,
    "title": "VM Information",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "source_vm internal IP address",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the source virtual machine",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Network/virtualNetworks/{resourcename}/virtualMachines/$ref?api-version=2017-09-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of VM's",
                    "text": "Unable to get the list of VM's"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "destination_vm internal IP address",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the destination Virtual Machine internal IP address",
            "watermarkText": "Enter destination Virtual Machine",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
