<properties
	pageTitle="Storage File Sync"
	description="Storage File Sync scoping question"
	authors="kartikshah9"
    ms.author="kashah"
	articleId="StorageScoping_file_sync"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32675720,32675721,32675722,32675724,32675725,32675726"
	productPesIds="16460"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_StorageFiles"
/>
# Storage File Sync scoping question
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage File Sync scoping question",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure File Sync Errors - Troubleshooting and Remediation",
        "description": "The Azure File Sync troubleshooter can help remediate File sync issues. Use the below diagnostic to search the file sync error observed in the portal. For example search error code 0x8007007B",
        "insightNotAvailableText": "Our troubleshooter did not identify remediation for your issue. See the recommended documentation link to troubleshoot your issue"
    },
    "formElements": [
        {
            "id": "file_sync",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "File Sync resource",
            "watermarkText": "Choose a File Sync",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.StorageSync/storageSyncServices?api-version=2018-04-02",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "DropdownOptions": [
                {
                    "value": "NoFileSync",
                    "text": "Not specific to a File Sync"
                }
            ],
            "required": true
        },
        {
            "id": "syncgroup",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Sync Group Name",
            "watermarkText": "Enter Sync Group Name or else enter Not Applicable",
            "required": true
        },
        {
            "id": "filesyncerrors",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "File Sync errors",
            "watermarkText": "Search File Sync error. Example search 0x8007007B",
            "dropdownOptions": [
                {
                    "value": "0x80C8300F",
                    "text": "0x80C8300F     ECS_E_REPLICA_NOT_READY"
                },
                {
                    "value": "0x80C8021C",
                    "text": "0x80C8021C     ECS_E_SYNC_METADATA_KNOWLEDGE_LIMIT_REACHED"
                },
                {
                    "value": "0x80C80253",
                    "text": "0x80C80253     ECS_E_TOO_MANY_PER_ITEM_ERRORS"
                },
                {
                    "value": "0x8007007B",
                    "text": "0x8007007B     ERROR_INVALID_NAME"
                },
                {
                    "value": "0x80C8031A",
                    "text": "0x80C8031A     ECS_E_NOT_ENOUGH_LOCAL_STORAGE"
                },
                {
                    "value": "0x80C8603E",
                    "text": "0x80C8603E     ECS_E_AZURE_STORAGE_SHARE_SIZE_LIMIT_REACHED"
                },
                {
                    "value": "0x8E5E0211",
                    "text": "0x8E5E0211     JET_errLogDiskFull"
                },
                {
                    "value": "0x800704C7",
                    "text": "0x800704C7     ERROR_CANCELLED"
                },
                {
                    "value": "0x80C8306B",
                    "text": "0x80C8306B     ECS_E_AGENT_VERSION_BLOCKED"
                },
                {
                    "value": "0x80072EE7",
                    "text": "0x80072EE7     WININET_E_NAME_NOT_RESOLVED"
                },
                {
                    "value": "0x80C8033E",
                    "text": "0x80C8033E     ECS_E_SERVER_BLOCKED_BY_NETWORK_ACL"
                },
                {
                    "value": "0x80C83088",
                    "text": "0x80C83088     ECS_E_INVALID_AAD_TENANT"
                },
                {
                    "value": "0x8E5E044E",
                    "text": "0x8E5E044E     JET_errWriteConflict"
                },
                {
                    "value": "0x80C8305F",
                    "text": "0x80C8305F     ECS_E_EXTERNAL_STORAGE_ACCOUNT_AUTHORIZATION_FAILED"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
             "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "watermarkText": "If applicable, please provide sync group name, server endpoint name, cloud endppoint, and error message.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
