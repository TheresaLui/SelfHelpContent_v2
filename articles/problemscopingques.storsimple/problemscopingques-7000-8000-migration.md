<properties
	articleId="01d9d342-3648-4876-ab5f-9b7b137993c6"
	pageTitle="Scoping for 7000-8000 Migration"
	description="7000-8000 Migration Scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630491"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Scoping for 7000-8000 Migration
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "7000-8000 Migration",
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
            "id": "software version",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the source appliance software version",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Version 2.1.1.518",
                    "text": "Version 2.1.1.518"
                },
                {
                    "value": "Version 2.1.1.548",
                    "text": "Version 2.1.1.548"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "serial number",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Serial number of source appliance",
            "watermarkText": "Serial number of 5000-7000 series source appliance",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
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
