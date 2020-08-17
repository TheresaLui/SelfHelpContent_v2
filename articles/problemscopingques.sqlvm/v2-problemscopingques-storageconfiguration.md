<properties
  pageTitle="Storage Configuration"
  description="Storage Configuration"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740103"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT" 
  schemaVersion="1"
  articleId="bc906a44-ab58-40a3-aba3-0be5bf6c5187"
  ownershipId="AzureData_AzureSQLVM"
/>
# Storage Configuration
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "My problem is not listed above",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "virtualdisk_scenario",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which of the following describes your scenario?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I want help with my Guest OS volume",
                    "text": "I want help with my Guest OS volume"
                },
                {
                    "value": "My data inside the temporary drive is lost",
                    "text": "My data inside the temporary drive is lost"
                },
                {
                    "value": "I want to find an availability set ID or use an availability set ID to get storage accounts",
                    "text": "I want to find an availability set ID or use an availability set ID to get storage accounts"
                },
                {
                    "value": "I want to find data about a managed disk",
                    "text": "I want to find data about a managed disk"
                },
                {
                    "value": "I want to find the provisioning status",
                    "text": "I want to find the provisioning status"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other (describe below)"
                }
            ],
            "required": false
        },
        {
            "id": "virtualdisk_task",
            "order": 2,
            "visibility": "virtualdisk_scenario == I want help with my Guest OS volume",
            "controlType": "dropdown",
            "displayLabel": "What is the task you are trying to perform?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Create or expand a storage pool configuration",
                    "text": "Create or expand a storage pool configuration"
                },
                {
                    "value": "Expand a Windows volume",
                    "text": "Expand a Windows volume"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other (describe below)"
                }
            ],
            "required": false
        },
        {
            "id": "virtualdisk_availabilityid_task",
            "order": 3,
            "visibility": "virtualdisk_scenario == I want to find an availability set ID or use an availability set ID to get storage accounts",
            "controlType": "dropdown",
            "displayLabel": "What is the task you are trying to perform?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Find an availability set ID",
                    "text": "Find an availability set ID"
                },
                {
                    "value": "Use an availability set ID to get storage accounts",
                    "text": "Use an availability set ID to get storage accounts"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other (describe below)"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
