<properties
    articleId="problemscopingques-sqlmi-conn-ts-errorcode"
    pageTitle="SQL Database Managed Instance"
    description="Scoping questions to capture managed instance issue when customer cannot connect"
    authors="vitomaz-msft,MladjoA"
    authoralias="vitomaz"
    ms.author="vitomaz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32746123,32746124,32746125,32746127"
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
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false
        },
        {
            "id": "source",
            "order": 3,
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
                    "value": "public_endpoint",
                    "text": "Using Public Endpoint"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Always provide the full error text from the underlying client library (e.g., SqlClient), not the general error from your client application. If available, include the client stack trace as well",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Obscure any personally identifiable information"
        },
        {
            "id": "driver_name",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "Driver or tool you are using?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": ".NET Framework",
                    "text": ".NET Framework"
                },
                {
                    "value": "ODBC driver",
                    "text": "ODBC driver"
                },
                {
                    "value": "PHP driver",
                    "text": "PHP driver"
                },
                {
                    "value": "JDBC driver",
                    "text": "JDBC driver"
                },
                {
                    "value": "Node.js driver",
                    "text": "Node.js driver"
                },
                {
                    "value": "OLEDB driver",
                    "text": "OLEDB driver"
                },
                {
                    "value": "SSMS",
                    "text": "SSMS"
                },
                {
                    "value": "SMO",
                    "text": "SMO"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ],
            "required": false
        },
        {
            "id": "driver_version",
            "order": 31,
            "controlType": "textbox",
            "displayLabel": "Version of the driver or tool?",
            "watermarkText": "Provide the version of your driver/tool",
            "required": false,
            "useAsAdditionalDetails": false
        }
    ]
}
---