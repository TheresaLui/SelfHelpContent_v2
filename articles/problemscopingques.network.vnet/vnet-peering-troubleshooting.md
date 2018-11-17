<properties
	pageTitle="VNET Peering Troubleshooting"
	description="VNET Peering Troubleshooting"
	authors="KristinaNeyens"
	selfHelpType="problemScopingQuestions"
	articleid="cannotconnectVMinapeeredVNET"
	supportTopicIds="32584249"
	productPesIds="15526"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# VNET Peering Troubleshooting
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
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of VM's",
                    "text": "Unable to get the list of VM's"
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
        }
    ]
}
---
