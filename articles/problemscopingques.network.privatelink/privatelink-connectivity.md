<properties
    pageTitle="Private Link connectivity"
    description="Private Link connectivity"
    authors="ramandhillon84"
    ms.author="rdhillon"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32681488"
    productPesIds="16843"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="700961cc-d014-4545-be70-2069dc2e0107"
	ownershipId="CloudNet_PrivateLink"
/>

# Private Link - connectivity 
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Private Link connectivity",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "destination_service",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the destination service for your Private Link",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Storage",
                    "text": "Azure Storage"
                },
                {
                    "value": "Azure Data Lake Storage Gen 2",
                    "text": "Azure Data Lake Storage Gen 2"
                },
                {
                    "value": "Azure SQL Database",
                    "text": "Azure SQL Database"
                },
                {
                    "value": "Azure SQL Data Warehouse",
                    "text": "Azure SQL Data Warehouse"
                },
                {
                    "value": "Azure Cosmos DB",
                    "text": "Azure Cosmos DB"
                },
                {
                    "value": "Azure Database for PostgreSQL - Single Server",
                    "text": "Azure Database for PostgreSQL - Single Server"
                },
                {
                    "value": "Azure Database for MySQL",
                    "text": "Azure Database for MySQL"
                },
                {
                    "value": "Azure Database for MariaDB",
                    "text": "Azure Database for MariaDB"
                },
                {
                    "value": "Custom Private Link Service behind Azure Standard Load Balancer",
                    "text": "Custom Private Link Service behind Azure Standard Load Balancer"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "source_location",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Please select the source from where you are accessing Private Link",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Virtual Network",
                    "text": "Virtual Network"
                },
                {
                    "value": "Virtual Network Peering",
                    "text": "Virtual Network Peering"
                },
                {
                    "value": "On-premises site",
                    "text": "On-premises site"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "dns_usage",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Please select the type of DNS usage",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Private DNS Zone",
                    "text": "Azure Private DNS Zone"
                },
                {
                    "value": "Custom DNS",
                    "text": "Custom DNS"
                },
                {
                    "value": "Both",
                    "text": "Both"
                },
                {
                    "value": "Neither",
                    "text": "Neither"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
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
            "displayLabel": "Please specify any additional details or questions",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "What is your specific connectivity scenario with Private Link Service?"
                },
                {
                    "text": "Did you receive any error messages? (If yes, please share the error message as well)"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---