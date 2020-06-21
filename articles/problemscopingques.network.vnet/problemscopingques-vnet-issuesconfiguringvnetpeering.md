<properties
	pageTitle="Issues configuring VNet Peering"
	description="Issues configuring VNet Peering"
	authors="anavinahar"
    ms.author="anavin"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32589558"
	productPesIds="15526"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="13819438614"
	ownershipId="CloudNet_VirtualNetwork"
/>
# Issues configuring VNet Peering
---
{
    "resourceRequired": true,
    "title": "Issues configuring VNet Peering",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "cannot_connect_vm",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the source virtual network you are experiencing connectivity issues with",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Network/virtualNetworks/{resourcename}/$ref?api-version=2017-09-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of virtual networks",
                    "text": "Unable to get the list of virtual networks"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 2,
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
                    "text": " "
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
