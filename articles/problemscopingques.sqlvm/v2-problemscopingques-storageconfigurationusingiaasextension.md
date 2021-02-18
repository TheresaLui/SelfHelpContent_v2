<properties
  pageTitle="Storage Configuration using Iaas Extension"
  description="Storage Configuration using Iaas Extension"
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
# Storage Configuration using Iaas Extension
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "My problem is not listed above",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "virtualdisk_scenario",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which of the following describes your scenario?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I want help with extending my disk",
                    "text": "I want help with my Guest OS volume"
                },
                {
                    "value": "My data inside the temporary drive is lost",
                    "text": "My data inside the temporary drive is lost"
                },
                {
                    "value": "Extending disk using Storage Configuration from SQL Virtual Machine Resource Fails",
                    "text": "Extending disk using Storage Configuration from SQL Virtual Machine Resource Fails"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other (describe below)"
                }
            ],
            "required": true
        },
        {
            "id": "virtualdisk_task",
            "order": 3,
            "visibility": "virtualdisk_scenario == I want help with extending my disk",
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
                    "value": "dont_know_answer",
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
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
