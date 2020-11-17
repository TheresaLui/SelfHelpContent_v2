<properties
	articleId="757e20d7-b058-4b34-906f-e7d2ed19eed3"
	pageTitle="Scoping slow reads and writes"
	description="Slow reads and writes scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630506"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Slow reads and writes
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Slow reads and writes",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "storsimple_devices",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "Device name",
            "watermarkText": "Choose an option",
            "required": false,
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/Microsoft.StorSimple/managers/{resourceName}/devices?&api-version=2017-06-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No devices available"
                }
            }
        },
        {
            "id": "volume_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of volumes are observing slowness",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Tiered volumes",
                    "text": "Tiered volumes"
                },
                {
                    "value": "Locally pinned volumes",
                    "text": "Locally pinned volumes"
                }
            ],
            "required": false
        },
        {
            "id": "cloud_bandwidth",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Specify the cloud bandwidth available to StorSimple",
            "watermarkText": "Cloud bandwidth in Mbps",
            "required": false
        },
        {
            "id": "dedicated_or_shared",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the cloud bandwidth dedicated or shared?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Dedicated",
                    "text": "Dedicated"
                },
                {
                    "value": "Shared",
                    "text": "Shared"
                }
            ],
            "required": false
        },
        {
            "id": "mpio",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is MPIO configured on the servers where the volume is hosted?",
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
            "id": "antivirus",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "If antivirus is configured on the file server, what kind of scanning is performed?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Full scan",
                    "text": "Full scan"
                },
                {
                    "value": "Scan on open and close",
                    "text": "Scan on open and close"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 8,
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
