<properties
	articleId="a6fef229-a889-43ca-bee0-85dbd8952751"
	pageTitle="Scoping cannot create cloud appliance"
	description="Cannot create cloud appliance"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630503"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Can't create a cloud appliance
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Cannot create a cloud appliance",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "slow_vm_determination",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the model of cloud appliance that is being created",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "8010",
                    "text": "8010"
                },
                {
                    "value": "8020",
                    "text": "8020"
                }
            ],
            "required": false
        },
        {
            "id": "region",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the region in which the cloud appliance is being deployed?",
            "watermarkTest": "Azure region",
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
