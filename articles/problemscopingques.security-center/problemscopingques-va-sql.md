<properties
	pageTitle="Azure Defender - Vulnerability Assessment (VA) - SQL vulnerability assessment"
	description="Azure Defenderr - Vulnerability Assessment (VA) - SQL vulnerability assessment"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32749422"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_asc_va_sql"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Configuring Features and Resources - Just-in-time access (JIT)
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Vulnerability Assessment (VA) - SQL vulnerability assessment",
				"subscriptionRequired": false,
                "formElements": [
                {
                    "id": "issue_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Select the issue you're requesting support for",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Enabling Azure Defender for SQL",
                            "text": "Enabling Azure Defender for SQL"
                        },
                        {
                            "value": "Pricing of Azure Defender for SQL",
                            "text": "Pricing of Azure Defender for SQL"
                        },
                        {
                            "value": "VA for Azure Defender for SQL",
                            "text": "VA for Azure Defender for SQL"
                        },
                        {
                            "value": "ATP for Azure Defender for SQL",
                            "text": "ATP for Azure Defender for SQL"
                        },                        {
                            "value": "dont_know_answer",
                            "text": "Other"
                        }
                    ],
                    "required": true
                },{
                    "id": "issue_location",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "SQL server type",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Azure SQL server/database (PaaS)",
                            "text": "Azure SQL server/database (PaaS)"
                        },
                        {
                            "value": "Azure SQL servers VMs (IaaS)",
                            "text": "Azure SQL servers VMs (IaaS)"
                        },
                        {
                            "value": "SQL servers On-Premises",
                            "text": "SQL servers On-Premises"
                        },
                        {
                            "value": "dont_know_answer",
                            "text": "Other"
                        }
                    ],
                    "required": true
                },{
                    "id": "problem_description",
                    "order": 1,
                    "controlType": "multilinetextbox",
                    "displayLabel": "Description",
                    "useAsAdditionalDetails": true,
                    "required": true
                    },{
                    "id": "problem_start_time",
                    "order": 8,
                    "controlType": "datetimepicker",
                    "displayLabel": "When did the problem start?",
                    "required": true
                  }
                  ]
}
---
