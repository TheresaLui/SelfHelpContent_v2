<properties
    articleId="problemscopingques-sqlmi-conn-ts-18456"
    pageTitle="SQL Database Managed Instance"
    description="Scoping questions to capture managed instance issue when customer cannot connect"
    authors="vitomaz-msft,MladjoA"
    authoralias="vitomaz"
    ms.author="vitomaz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32746123,32746114"
    productPesIds="16259"
    cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
    schemaVersion="1"
    ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "SQL Database Managed Instance",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Failed Login Troubleshooter",
        "description": "The Failed Login Troubleshooter can identify the cause of many common failed login errors.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "auth_method",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What authentication method you are using?",
            "required": true,
            "watermarkText": "Authentication method",
            "infoBalloonText": "Choose the authentication method you are using",
            "dropdownOptions": [
                {
                    "text": "SQL Server Authentication",
                    "value": "SQL"
                },
                {
                    "text": "Application token authentication",
                    "value": "Token"
                },
                {
                    "text": "Azure Active Directory Password",
                    "value": "AADPassword"
                },
                {
                    "text": "Azure Active Directory Integrated",
                    "value": "AADIntegrated"
                },
                {
                    "text": "Azure Active Directory Universal with Multi-Factor Authentication",
                    "value": "AADUniversalMFA"
                },
                {
                    "text": "Don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ],
            "dynamicDropdownOptions": null,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "database_name",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What database is having issues?",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "{resourceid}/databases?api-version=2017-03-01-preview",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of databases",
                    "text": "Unable to get the list of databases"
                }
            ],
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "source",
            "order": 4,
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