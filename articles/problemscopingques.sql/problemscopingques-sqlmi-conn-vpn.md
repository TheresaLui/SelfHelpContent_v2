<properties
	articleId="problemscopingques-sqlmi-conn-vpn"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to vpn or express route driver related issues"
	authors="vitomaz-msft,MladjoA"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32637262"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	schemaVersion="1"
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
            "displayLabel": "Where are you trying to connect from?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "same_vnet",
                    "text": "Application inside the same VNet"
                },
                {
                    "value": "vnet_peering_same_region",
                    "text": "Application in a different VNet, using Azure Virtual Network peering, both in same region"
                },
                {
                    "value": "vnet_peering_different_region",
                    "text": "Application in a different VNet, using Azure Virtual Network peering, in different regions"
                },
                {
                    "value": "vnet_gateway",
                    "text": "Application in a different VNet, using VNet-to-VNet VPN gateway"
                },
                {
                    "value": "on_prem_site_to_site",
                    "text": "On-premises application, using Site-to-Site VPN connection"
                },
                {
                    "value": "on_prem_point_to_site",
                    "text": "On-premises application, using Point-to-Site VPN connection"
                },
                {
                    "value": "on_prem_expressroute",
                    "text": "On-premises application, using ExpressRoute connection"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
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