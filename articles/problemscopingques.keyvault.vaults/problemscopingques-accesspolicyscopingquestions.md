<properties
         pageTitle="Access Policy scoping questions for Key Vault support requests."
         description="Access Policy scoping questions for Key Vault support requests."
         authors="ShaneBala-keyvault"
         ms.author="sudbalas"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32783952, 32596880, 32743815"
         productPesIds="15657"
         schemaVersion="1"
         articleId="problemscopingques-accesspolicyscopingquestions"
	     cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	     ownershipId="AzureKeyVault_KeyVault"
/>
# Service Principal Cannot Access Key Vault
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Service Principal Cannot Access Key Vault",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "new_spn",
            "order": 1,
            "controlType": "radioButtonGroup",
            "displayLabel": "Are you attempting to configure access for a new user or application? Choose the best answer.",
            "radioButtonOptions": [{
                    "value": "yes",
                    "text": "Yes, I am configuring a new service principal."
                }, {
                    "value": "no",
                    "text": "No, I am experiencing an issue with a previously configured service principal."
                }
            ],
            "required": true
        },
        {
            "id": "recurring_issue",
            "order": 2,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is this an intermittent issue?",
            "radioButtonOptions": [{
                    "value": "yes",
                    "text": "Yes, operations sometimes succeed but the service principal experiences regular failures. Choose the best answer."
                }, {
                    "value": "no",
                    "text": "No, my service principal has no access to the key vault."
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did you start experiencing this issue?",
            "required": true
        },
	{
            "id": "key_vault_name",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the object id of your security principal?",
            "required": false
        },
        {
            "id": "spn_type",
            "order": 5,
            "controlType": "multiselectdropdown",
            "displayLabel": "What type of security principal are you trying to use?",
            "dropdownOptions": [{
                    "value": "User Principal (User)",
                    "text": "User Principal (User)"
                }, {
                    "value": "Service Principal (Application)",
                    "text": "Service Principal (Application)"
                }, {
                    "value": "Managed Service Identity (Azure Resource)",
                    "text": "Managed Service Identity (Azure Resource)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know answer"
                }
            ],
            "required": true
        },
        {
            "id": "spn_object_id",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the object id of your security principal?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "attached_screenshots",
            "order": 8,
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
            "order": 9,
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
            "order": 10,
            "visibility": "error_message_available == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Error message details",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
