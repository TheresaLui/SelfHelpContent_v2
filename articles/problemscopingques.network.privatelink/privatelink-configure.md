<properties
    pageTitle="Private Link configuration"
    description="Private Link configuration"
    authors="ramandhillon84"
    ms.author="rdhillon"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32681486"
    productPesIds="16843"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="700961cc-d014-4545-be70-2069dc2e0106"
	ownershipId="CloudNet_PrivateLink"
/>

# Private Link - configuration 
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Private Link configuration",
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
            "id": "config_goals",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Please select the operation that you need help with",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Create a new Private Link Service",
                    "text": "Create a new Private Link Service"
                },
                {
                    "value": "Update the existing Private Link Service",
                    "text": "Update the existing Private Link Service"
                },
                {
                    "value": "Manage Private Endpoint connections to an existing Private Link Service",
                    "text": "Manage Private Endpoint connections to an existing Private Link Service"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "slb_sku",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Please select your Azure Software Load Balancer SKU",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Standard SKU",
                    "text": "Standard SKU"
                },
                {
                    "value": "Basic SKU",
                    "text": "Basic SKU"
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
                    "text": "Do you need help with any specific configuration problem?"
                },
                {
                    "text": "Did you receive any error messages while configuring the Private Link Service? (If yes, please share the error message as well)"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
