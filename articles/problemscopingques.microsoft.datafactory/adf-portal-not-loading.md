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
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure Data Factory Portal not loading",
    "fileAttachmentHint": "Please attach screenshot of the browser",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please briefly describe the issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "browser_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which type of browser are you using?",
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
                    "value": "Unsupported",
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
            "displayLabel": "Are 3rd party cookies enabled on the browser?",
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
                    "value": "assistance",
                    "text": "I need assistance enabling this setting"
                }
            ],
            "required": true
        },
        {
            "id": "cache",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Have you tried clearing the browser cache?",
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
                    "value": "NA",
                    "text": "N/A"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
