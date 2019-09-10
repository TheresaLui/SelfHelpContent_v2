<properties
	pageTitle="Storage migration using AzCopy"
	description="Issues migrating data using AzCopy"
	authors="Passaree"
        ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602696,32630512"
	productPesIds="15629,16459"
	cloudEnvironments="public,MoonCake,FairFax"
	schemaVersion="1"
	articleId="321513E7-1346-42C6-A5BC-2D43DA486F20"
/>

# Storage migration between Storage Accounts
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issues migrating data using AzCopy",
    "fileAttachmentHint": "Upload AzCopy Log for fast case resolution. Log files are located in the %USERPROFILE\\\\.azcopy directory on Windows, or in the $HOME\\\\.azcopy",
    "diagnosticCard": {
        "title": "What caused AzCopy issue?",
        "description": "Our Data Migration AzCopy troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Please ensure the information provided is accurate and in the approved format. Also, see our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
          {
            "id": "storage_account_from",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Source storage account",
            "watermarkText": "Select storage account",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Storage/storageAccounts?api-version=2018-07-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "From a different subscription, external source or not applicable"
                }
            },
            "required": true
        },
	 {
            "id": "storage_account_to",
            "visibility": "true",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Destination storage account",
            "watermarkText": "Enter storage account name",
            "required": true
        },
	{
            "id": "azcopy_version",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Version of AzCopy you are using",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "AzCopy_above10.1",
                    "text": "v10.1.0 and above"
                },
                {
                    "value": "AzCopy_10_10.0.9",
                    "text": "v10.0.0 - 10.0.9"
                },
                {
                    "value": "AzCopy_below8.1",
                    "text": "v8.1 and below"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "azcopy_performance",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you experiencing any performance issue with the copy operations",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "no",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "error_code",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Did you receive any error code? ",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "error400",
                    "text": "400 - Bad Request"
                },
                {
                    "value": "error401",
                    "text": "401 – Unauthorized"
                },
                {
                    "value": "error403",
                    "text": "403 – Forbidden"
                },
                {
                    "value": "error404",
                    "text": "404 - Resource not found (Authentication)"
                },
                {
                    "value": "error409",
                    "text": "409 - Conflict"
                },
                {
                    "value": "error412",
                    "text": "412 – Precondition failed"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": false,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
