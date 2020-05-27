<properties
	pageTitle="Storage Firewall and VNet"
	description="Storage Firewall and VNet scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602697"
	productPesIds="15629"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="45381637-aa37-4dbf-81aa-529ab0d16599"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Storage Firewall and VNet
---
{
    "resourceRequired": false,
    "title": "Storage Firewall and VNet scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "application_type",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "If your service/application is not working after configuring Firewall, choose what was impacted",
            "watermarkText": "Choose what was impacted",
            "dropdownOptions": [
                {
                    "value": "Azure_Storage",
                    "text": "Azure Storage operations not working, e.g. disk import/export"
                },
                {
                    "value": "Azure_Internal",
                    "text": "Other Azure or Microsoft Services not working"
                },
                {
                    "value": "Azure_ThirdParty",
                    "text": "3rd party services running in Azure not working"
                },
                {
                    "value": "External_ThirdParty",
                    "text": "3rd party services running outside Azure not working"
                }
            ],
            "required": false
        },
        {
            "id": "application_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Name(s) of impacted service(s)/application(s)",
            "watermarkText": "service1;service2;service3",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
