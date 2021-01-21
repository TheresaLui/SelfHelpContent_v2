<properties
	pageTitle="Azure Data Factory - ADF Portal not Loading"
	description="Scoping questions for ADF Portal not Loading"
	authors="hecepeda"
	ms.author="hecepeda"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32629437"
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    articleId="adf-portal-not-loading.md"
	ownershipId="AzureData_DataFactory"
/>

# Azure Data Factory - Portal not loading

---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Data Factory Portal not loading",
    "fileAttachmentHint": "Please attach screenshot of the browser",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Briefly describe the issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "browser_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which browser are you using?",
            "watermarkText": "Choose Data Factory Version",
            "dropdownOptions": [
                {
                    "value": "Edge",
                    "text": "Microsoft Edge"
                },
                {
                    "value": "Chrome",
                    "text": "Google Chrome"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other unsupported browser"
                }
            ],
            "required": true
        },
        {
            "id": "browser_version",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the version of the browser?",
            "required": true
        },
        {
            "id": "cookies",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are third-party cookies enabled in the browser?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I need assistance enabling this setting"
                }
            ],
            "required": true
        },
        {
            "id": "cache",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Have you tried clearing the browser's cache?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": true
        },
        {
            "id": "allowed_site_list",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Have you added Adf.Azure.com to the allowed site list?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I need assistance enabling this setting"
                }
            ],
            "required": false
        },
        {
            "id": "inprivate",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Does it work in Incognito mode (Chrome) or InPrivate mode for Edge?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
