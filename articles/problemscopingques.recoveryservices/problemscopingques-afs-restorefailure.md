<properties
         pageTitle="Scoping questions for AFS restore failure"
         description="Scoping questions for AFS restore failure"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32599716"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="bb54b8e4-1278-4704-8d10-64df311673b1"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions AFS restore failure
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "AFS restore failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "storage_account_name",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which storage account(s) is experiencing the problem?",
            "watermarkText": "Enter the name of the storage account(s)",
	    "dynamicDropdownOptions": {
            "uri": "/subscriptions/{subscriptionid}/resources?api-version=2018-05-01&$filter=resourceType eq 'Microsoft.Storage/storageAccounts' or resourceType eq 'Microsoft.ClassicStorage/storageAccounts'",
            "jTokenPath": "value",
            "textProperty": "name",
            "valueProperty": "id",
            "textPropertyRegex": ".*",
	    "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Other, don't know or not applicable"
            }
          },
            "required": false
        },
        {
            "id": "fileshare_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the name(s) of the file shares whose restore is failing?",
            "watermarkText": "Enter file shares name(s) comma separated",
            "required": false
        },
        {
            "id": "restore_Type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which type of restore are you performing?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Original Location",
                    "text": "Original Location"
                },
                {
                    "value": "Alternate Location",
                    "text": "Alternate Location"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "jobID_Name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Enter the failed restore job Activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "error_code",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Provide the error code that are you seeing:",
            "watermarkText": "Example: UserErrorStorageAccountNotFound",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---
