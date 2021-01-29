<properties
    pageTitle="Security"
    description="Security"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32738655"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-mysql-security-dataencryption"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Security - Data Encryption
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Security Data Encryption",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "error",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "If an error was displayed, what was the error message (including operation ID from activity log, if any)?",
            "required": false
        },
        {
            "id": "issue",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What is the specific issue you are facing?",
            "dropdownOptions": [
                {
                    "value": "Issues with key vault during Initial Setup",
                    "text": "Issues with key vault during Initial Setup"
                },
                {
                    "value": "Database is in an inaccessible State",
                    "text": "Database is in an inaccessible State"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Provide your repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---