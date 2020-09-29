<properties
	pageTitle="Cannot delete a Virtual Network"
	description="Cannot delete a Virtual Network"
	authors="anavinahar"
    ms.author="anavin"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32584253"
	productPesIds="15526"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="8766b9f2-62d3-4dc0-8b81-597d2b0535edtsdh"
	ownershipId="CloudNet_VirtualNetwork"
/>

# Cannot delete virtual network

---
{
    "resourceRequired": true,
    "title": "Cannot delete a Virtual Network",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "cannot_connect_vm",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the Virtual Network you are unable to delete",
            "watermarkText": "Choose a Virtual Network",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Network/virtualNetworks/$ref?api-version=2017-09-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of Virtual Networks",
                    "text": "Unable to get the list of Virtual Networks"
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
            "displayLabel": "Please provide details about the errors you receive when you try to delete your virtual network",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
