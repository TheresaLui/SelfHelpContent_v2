<properties
	articleId="b9c9c342-d532-4ad3-a31b-2d50e929f4b8"
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
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Slow reads and writes",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "volume_type",
            "order": 1,
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
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Specify the cloud bandwidth available to StorSimple",
            "watermarkText": "Cloud bandwidth in Mbps",
            "required": false
        },
        {
            "id": "dedicated_or_shared",
            "order": 3,
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
            "order": 4,
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
            "order": 5,
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
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
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
