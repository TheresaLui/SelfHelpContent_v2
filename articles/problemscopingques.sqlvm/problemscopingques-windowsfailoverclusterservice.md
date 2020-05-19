<properties pageTitle="Windows Server Failover Cluster Service"
	 description="Windows Server Failover Cluster Service"
	 authors="yareyes"
     ms.author="yareyes"
	 selfHelpType="problemScopingQuestions"
	 supportTopicIds="32633530"
	 productPesIds="14745"
	 cloudEnvironments="public,fairfax, usnat, ussec"
	 schemaVersion="1"
	 articleId="f91689b3-d0fb-4d41-b2d0-c9ef39bf01ee"
	ownershipId="AzureData_AzureSQLVM"
/>
# Windows Server Failover Cluster Service
---
{
    "resourceRequired": false,
    "title": "Windows Server Failover Cluster Service",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "whichReplication",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What operation do you need assistance with?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Create a Windows Server Failover Cluster",
                    "value": "CreateWsfc"
                },
                {
                    "text": "Manage existing Windows Server Failover Cluster",
                    "value": "ManageExistingWsfc"
                },
                {
                    "text": "Troubleshoot cluster performance problems",
                    "value": "TroubleshootPerfWsfc"
                },
                {
                    "text": "I’m not sure/don’t know",
                    "value": "dont_know_answer"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
