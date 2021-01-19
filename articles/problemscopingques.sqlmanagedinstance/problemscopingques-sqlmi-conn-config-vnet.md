<properties
	articleId="problemscopingques-sqlmi-conn-config-vnet"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to virtual network or subnet configuration"
	authors="vitomaz-msft,MladjoA"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32748006"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "SQL Database Managed Instance",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "source",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Where is your application/tool trying to connect from?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "same_vnet",
                    "text": "The same VNet hosting Managed Instance"
                },
                {
                    "value": "vnet_same_region",
                    "text": "Another VNet in the same region"
                },
                {
                    "value": "vnet_another_region",
                    "text": "VNet in another region"
                },
                {
                    "value": "onprem",
                    "text": "On-premises"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "source_details",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details about the source",
            "watermarkText": "If applicable, please provide the Subscription Id, VNet name, Subnet name and/or any other relevant information",
            "required": false
        },
        {
            "id": "source_details_same_vnet",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "How is source location connected with VNet hosting Managed Instance?",
            "watermarkText": "Choose an otion",
            "visibility": "source == vnet_same_region || source == vnet_another_region || source == dont_know_answer",
            "dropdownOptions": [
                {
                    "value": "peering",
                    "text": "VNet peering"
                },
                {
                    "value": "gateway",
                    "text": "VNet-to-VNet VPN gateway"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "source_details_onprem",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "How is source location connected with VNet hosting Managed Instance?",
            "watermarkText": "Choose an otion",
            "visibility": "source == onprem || source == dont_know_answer",
            "dropdownOptions": [
                {
                    "value": "site2site",
                    "text": "Site-to-Site VPN connection"
                },
                {
                    "value": "point2site",
                    "text": "Point-to-Site VPN connection"
                },
                {
                    "value": "express_route",
                    "text": "Express Route connection"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---