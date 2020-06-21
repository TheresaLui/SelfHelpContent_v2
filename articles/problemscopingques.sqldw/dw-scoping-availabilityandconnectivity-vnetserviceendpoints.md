<properties
	articleId="dw-scoping-availabilityandconnectivity-vnetserviceendpoints.md"
	pageTitle="VNET service endpoints"
	description="VNET service endpoints"
	authors="mlee3gsd"
	ms.author="martinle"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635232"
	productPesIds="15818"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_SQLDataWarehouse"
/>
# Availability and Connectivity - VNET service endpoints
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "VNET service endpoints",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "dw_scoping_availability_storageaccount",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "If you are connecting to a storage account, is the storage account on a VNet?",
            "required": false
        },
        {
            "id": "dw_scoping_availability_msi",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "If your storage account is on a VNet, are you using a Managed Service Identity (MSI)?",
            "required": false
        },
        {
            "id": "dw_scoping_availability_rbac",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What are the permissions on the storage account for the Managed Service Identity (MSI)?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---