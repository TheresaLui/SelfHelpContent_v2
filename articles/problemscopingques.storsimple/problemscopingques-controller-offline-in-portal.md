<properties
	articleId="eceebe10-2572-4f50-b83c-d759978a1061"
	pageTitle="Scoping for controller offline in portal"
	description="Controller offline in portal scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630497"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Controller offline in protal
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Slow virtual machine",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "controller",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the controller that is shown offline",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Controller 0",
                    "text": "Controller 0"
                },
                {
                    "value": "Controller 1",
                    "text": "Controller 1"
                }
            ],
            "required": false
        },
        {
            "id": "serial_access",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Do you have access to the device through the serial console",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
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
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
