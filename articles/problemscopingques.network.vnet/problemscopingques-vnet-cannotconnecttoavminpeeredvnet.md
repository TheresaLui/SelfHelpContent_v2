<properties
	pageTitle="Cannot connect to a VM in a peered VNet"
	description="Cannot connect to a VM in a peered VNet"
	authors="ritup"
    ms.author="anavin"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32584249"
	productPesIds="15526"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="8766b9f2-62d3-4dc0-8b81-597d2b0535ed"
/>
# Cannot Connect to or from Internet
---
{
    "resourceRequired": true,
    "title": "Cannot Connect to or from Internet",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "cannot_connect_vm",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the source VM you are experiencing connectivity issues with",
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
                    "text": "Are you trying to connect to or from the internet?"
                },
                {
                    "text": "Are you able to connect or ping another VM in the same VNet?"
                }
            ]
        }
    ]
}
---