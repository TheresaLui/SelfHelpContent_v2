<properties
	articleId="3e78500e-ee07-4b84-b009-8dfc62828cc4"
	pageTitle="Scoping unable to configure appliance"
	description="Unable to configure appliance"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630502"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Unable to configure device
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Unable to configure device",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "device_task",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which device-level configuration task is failing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Modification of device friendly name",
                    "text": "Modification of device friendly name"
                },
                {
                    "value": "Modification of device time settings",
                    "text": "Modification of device time settings"
                },
                {
                    "value": "Assignment of secondary DNS",
                    "text": "Assignment of secondary DNS"
                },
                {
                    "value": "Modification of network interfaces",
                    "text": "Modification of network interfaces"
                },
                {
                    "value": "Reassignment of IPs",
                    "text": "Reassignment of IPs"
                }
            ],
            "required": false
        },
        {
            "id": "port",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is port 9354 open on Data0 IPs?",
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
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Include output."
                },
                {
                    "text": "Run `invoke-hcsdiagnostics -scope network` and provide output below to assist in troubleshooting the issue."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
