<properties
	pageTitle="How to create rules in an existing NSG"
	description="How to create rules in an existing NSG"
	authors="anavinahar"
    ms.author="anavin"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32584257"
	productPesIds="15526"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="66574748238"
/>

# Cannot Connect to or from Internet

---
{
    "resourceRequired": true,
    "title": "How to create rules in an existing NSG",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "create_rules_existing_NSG",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the NSG you are experiencing connectivity issues with",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Network/virtualNetworks/{resourcename}/networkSecurityGroups/$ref?api-version=2018-11-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of NSGs",
                    "text": "Unable to get the list of NSGs"
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
            "displayLabel": "Please provide the on-premise IP address",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---