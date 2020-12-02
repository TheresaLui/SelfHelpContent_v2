<properties
         pageTitle="Recovery scoping questions for Key Vault support requests."
         description="Recovery scoping questions for Key Vault support requests."
         authors="ShaneBala-keyvault"
         ms.author="sudbalas"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32596891"
         productPesIds="15657"
         schemaVersion="1"
         articleId="problemscopingques-recoveryscopingquestions"
	     cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	     ownershipId="AzureKeyVault_KeyVault"
/>
# Troubleshooting Key Vault Recovery Features
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Troubleshooting Key Vault Recovery Features",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "scope_issue",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "What type of issue are you experiencing?",
            "dropdownOptions": [{
                    "value": "I get a conflict error when creating a key vault or key vault object",
                    "text": "I get a conflict error when creating a key vault or key vault object"
                },
                {
                    "value": "I need to recover a deleted key vault or key vault object",
                    "text": "I need to recover a deleted key vault or key vault object"
                },
                {
                    "value": "I am trying to turn off or modify a key vault recovery feature",
                    "text": "I am trying to turn off or modify a key vault recovery feature"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I am not sure"
                }
            ],
            "required": true
        },
        {
            "id": "key_vault_name",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the name of the key vault?",
            "required": true
        },
        {
            "id": "soft_delete_enabled",
            "order": 3,
            "controlType": "radioButtonGroup",
            "displayLabel": "Does this key vault have soft delete enabled?",
            "radioButtonOptions": [{
                    "value": "yes",
                    "text": "Yes, This key vault has soft delete enabled."
                }, {
                    "value": "no",
                    "text": "No, This key vault does not have soft delete enabled."
                },
                {
                    "value": "not sure",
                    "text": "I'm not sure"
                }
            ],
            "required": true
        },
        {
            "id": "purge_protection_enabled",
            "order": 4,
            "controlType": "radioButtonGroup",
            "displayLabel": "Does this key vault have purge protection enabled?",
            "radioButtonOptions": [{
                    "value": "yes",
                    "text": "Yes, This key vault has purge protection enabled."
                }, {
                    "value": "no",
                    "text": "No, This key vault does not have purge protection enabled."
                },
                {
                    "value": "not sure",
                    "text": "I'm not sure"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did you start experiencing this issue?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "acknowledge_limitation_A",
            "order": 7,
            "controlType": "radioButtonGroup",
            "displayLabel": "I acknowledge that Microsoft is not able to recover deleted key vaults or objects if soft delete was not enabled or the retention period has elapsed.",
            "radioButtonOptions": [{
                    "value": "yes",
                    "text": "Yes"
                }
            ],
            "required": true
        },
        {
            "id": "acknowledge_limitation_B",
            "order": 8,
            "controlType": "radioButtonGroup",
            "displayLabel": "I acknowledge that Microsoft is not able to modify or disable key vault recovery features on my behalf.",
            "radioButtonOptions": [{
                    "value": "yes",
                    "text": "Yes"
                }
            ],
            "required": true
        },
        {
            "id": "attached_screenshots",
            "order": 9,
            "controlType": "radioButtonGroup",
            "displayLabel": "Are screenshots attached:",
            "radioButtonOptions": [{
                    "value": "yes",
                    "text": "Yes"
                }, {
                    "value": "no",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "error_message_available",
            "order": 10,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is there an error message?",
            "radioButtonOptions": [{
                    "value": "Yes",
                    "text": "Yes"
                }, {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "error_message_description",
            "order": 11,
            "visibility": "error_message_available == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Error message details",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
