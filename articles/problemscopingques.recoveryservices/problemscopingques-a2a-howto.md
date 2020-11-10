<properties
         pageTitle="Scoping questions for Azure VM disaster recovery advisory"
         description="Scoping questions for Azure VM disaster recovery advisory"
         authors="genlin"
         ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32630515"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="2b342a85-2011-9011-7171-43639892e013"
	ownershipId="Compute_SiteRecovery"
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
                    "value": "IP address assignment during failover",
                    "text": "IP address assignment during failover"
                },
                {
                    "value": "Azure VM disaster Recovery Cost",
                    "text": "Azure VM disaster Recovery total cost"
                },
                {
                    "value": "what all Azure Site recovery replicates to the Disaster Recovery region",
                    "text": "Which resources can be replicated to the Disaster Recovery region"
                },
                {
                    "value": "recovery points generation",
                    "text": "Recovery points generation"
                },
                {
                    "value": "deleting Azure Site recovery artifacts",
                    "text": "Cleaning up stale Site Recovery resources"
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
            "displayLabel": "Select the docs.microsoft.com articles that you have consulted",
            "dropdownOptions": [
                {
                    "value": "Azure to Azure disaster recovery common queries",
                    "text": "Common questions: Azure-to-Azure disaster recovery"
                },
                {
                    "value": "Azure to Azure dr architecture document",
                    "text": "Azure to Azure disaster recovery architecture"
                },
                {
                    "value": "have gone through Azure to Azure supported region lists",
                    "text": "Support matrix for replicating Azure VMs from one region to another"
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
    ],
    "$schema": "SelfHelpContent"
}
---
