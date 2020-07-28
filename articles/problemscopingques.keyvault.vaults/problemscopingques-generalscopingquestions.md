<properties
         pageTitle="General scoping question for Key Vault support requests."
         description="General scoping question for Key Vault support requests."
         authors="osmuller"
         ms.author="osmuller"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32739887,32739888,32739889,32739890,32739891,32739892,32739893,32738119,32375283,32375284,32375287,32375288,32375291,32738120,32452742,32743817,32596891,32375296,32375297,32738115,32375295,32596890,32596880,32743814,32743815,32596879,32743816,32596882,32596884,32375292,32375293,32738117,32739894,32596886,32738116,32742808,32742809,"
         productPesIds="15657"
         schemaVersion="1"
         articleId="problemscopingques-generalscopingquestions"
	     cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	     ownershipId="AzureKeyVault_KeyVault"
/>
# Vault cannot be found
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Vault cannot be found",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Incident time",
            "required": true
        },
        {
            "id": "expected_experience",
            "order": 2,
            "visibility": "null",
            "controlType": "multilinetextbox",
            "displayLabel": "What is the expected experience and how does that differ from the actual result?",
            "required": false,
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "attached_screenshots",
            "order": 4,
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
            "id": "application_environment",
            "order": 5,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the environments that are running your applications",
            "dropdownOptions": [{
                    "value": "Virtual Machine",
                    "text": "Virtual Machine"
                }, {
                    "value": "App Service",
                    "text": "App Service"
                }, {
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know answer"
                }
            ],
            "required": true
        },
        {
            "id": "other_application_environment",
            "visibility": "application_environment == Other",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Other Application Environment",
            "required": true
        },
        {
            "id": "error_message_available",
            "order": 7,
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
            "order": 8,
            "visibility": "error_message_available == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Error message details",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
