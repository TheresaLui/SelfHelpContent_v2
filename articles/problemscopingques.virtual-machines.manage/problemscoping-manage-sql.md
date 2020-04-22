<properties
                pageTitle="Management"
                description="Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32411820"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0095"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Manage an instance of SQL Server",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "manage_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "manage_issue",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "What is/are the primary issue(s) you are facing with SQL Server?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Need help with installation",
                    "text": "Need help with installation"
                },
                {
                    "value": "Always on setup",
                    "text": "Always on setup"
                },
                {
                    "value": "Unable to connect to SQL server instance",
                    "text": "Unable to connect to SQL server instance"
                },
                {
                    "value": "Help in migrating from on-premise to Azure VM",
                    "text": "Help in migrating from on-premise to Azure VM"
                },
                {
                    "value": "SQL job related issues",
                    "text": "SQL job related issues"
                },
                {
                    "value": "User authentication issues",
                    "text": "User authentication issues"
                },
                {
                    "value": "Backup/Restore issues",
                    "text": "Backup/Restore issues"
                },
                {
                    "value": "Slow query performance issues",
                    "text": "Slow query performance issues"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
