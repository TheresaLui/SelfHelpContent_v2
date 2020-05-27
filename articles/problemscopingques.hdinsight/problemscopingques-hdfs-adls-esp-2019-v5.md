<properties
	articleId="bb84ca9c-05b3-437a-a5e4-49812c98d489"
	pageTitle="Scoping Questions for HDInsight HDFS ADLS Gen 1 or 2 in ESP Issue"
	description="Scoping Questions for HDInsight HDFS ADLS Gen 1 or 2 in ESP Issue"
	authors="shravanmn, csunilkumar, lisaliu"
	ms.author="shravan, sunilkc, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636434"
	productPesIds="15078"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_HDInsight"
/>
# HDInsight HDFS ADLS Gen 1 or 2 in ESP Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "HDInsight HDFS ADLS Gen 1 or 2 in ESP Issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        },
        {
            "id": "aadcredential",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Have you kinited or logged in using AAD credential?",
            "watermarkText": "Choose an option",
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
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "hdfs-ls-work",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Does hdfs dfs -ls / work?",
            "watermarkText": "Choose an option",
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
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "hdfs-error",
            "order": 5,
            "visibility": "hdfs-ls-work == No",
            "controlType": "textbox",
            "displayLabel": "hdfs dfs -ls error message",
            "required": false
        },
        {
            "id": "gatewayorscript",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Have you logged in to Ambari through the gateway or run the RegisterKerbTicketAndOAuth.sh script?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Gateway",
                    "text": "Through Gateway"
                },
                {
                    "value": "Script",
                    "text": "Run the RegisterKerbTicketAndOAuth.sh script"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "storage_type",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "Is storage affected the primary or secondary storage account",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "primary",
                    "text": "Primary storage account"
                },
                {
                    "value": "secondary",
                    "text": "Secondary storage account"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "changes_category",
            "order": 40,
            "controlType": "dropdown",
            "displayLabel": "Any change made to any of these components?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "HDInsight_cluster",
                    "text": "HDInsight cluster configuration"
                },
                {
                    "value": "reboot",
                    "text": "Node or service reboot"
                },
                {
                    "value": "Network",
                    "text": "Network"
                },
                {
                    "value": "Storage_account",
                    "text": "Storage account"
                },
                {
                    "value": "access",
                    "text": "Password, access key, or certificate rotation"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "changes_detail",
            "visibility": "changes_category != dont_know_answer",
            "order": 50,
            "controlType": "multilinetextbox",
            "displayLabel": "Detail of the changes",
            "watermarkText": "Please describe the changes in detail",
            "required": false
        },
        {
            "id": "mitigation",
            "order": 200,
            "controlType": "multilinetextbox",
            "displayLabel": "Mitigating actions taken so far",
            "watermarkText": "Any mitigating actions taken so far and the result",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 500,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detail symptom including the full error text, exception callstack if available, whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
