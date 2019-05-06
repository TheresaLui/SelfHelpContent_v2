<properties
         pageTitle="Scoping questions for Azure VM disaster recovery advisory"
         description="Scoping questions for Azure VM disaster recovery advisory"
         authors="genlin"
         ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32630515"
         productPesIds="16370"
         cloudEnvironments="public"
         schemaVersion="1"
         articleId="2b342a85-2011-9011-b7d0-43639892e013"
/>
# Questions Azure VM protection failure 
---
{
   "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure VM configuration failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "Select_ErrorMessage",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which topic do you want to know about?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Site recovery support of new operating systems and kernel version",
                    "text": "Operating systems and kernel versions that Site Recovery supports"
                },
                {
                    "value": "IP address assignment during Failover",
                    "text": "IP address assignment during Failover"
                },
                {
                    "value": "Azure VM disaster Recovery Cost",
                    "text": "Azure VM disaster Recovery total cost"
                },
                {
                    "value": "what all Azure Site recovery replicates to the Disaster Recovery region",
                    "text": "Replicate all resources to the Disaster Recovery region"
                },
                {
                    "value": "recovery points generation",
                    "text": "Recovery points generation"
                },
                {
                    "value": "deleting Azure Site recovery artifacts",
                    "text": "Delete Azure Site recovery artifacts"
                },
		{
		    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
		}
            ],
            "required": true
        },
        {
            "id": "Basic_troubleshooting_multiselect",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps you have completed",
            "dropdownOptions": [
                {
                    "value": "Read Azure to Azure disaster recovery common queries",
                    "text": "Azure to Azure disaster recovery common queries"
                },
                {
                    "value": "Azure to Azure dr architecture document",
                    "text": "azure to azure dr architecture document"
                },
                {
                    "value": "have gone through Azure to Azure supported region lists",
                    "text": "have gone through Azure to Azure supported region lists"
                },
		{
		    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
		}
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ]
}
---
