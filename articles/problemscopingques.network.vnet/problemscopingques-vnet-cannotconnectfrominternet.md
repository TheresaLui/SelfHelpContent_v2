<properties
	pageTitle="Cannot Connect to or from Internet"
	description="Cannot Connect to or from Internet"
	authors="ritup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32584250"
	productPesIds="15526"
	cloudEnvironments="public"
	schemaVersion="1"
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
            "displayLabel": "Please select the VM you are experiencing connectivity issues with",
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
