<properties
    pageTitle="V2A Replication not progressing"
    description="V2A Replication not progressing"
    authors="srinathv"
    ms.author="aaronmax"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32680615"
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="b90a41b2-0813-486c-9513-296f4bfcb416"
	ownershipId="Compute_SiteRecovery"
/>
# V2A Replication not progressing
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "V2A Replication not progressing",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_os_version",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What is the Operating System version (and kernel version for Linux) of the VM that you are trying to protect?",
            "watermarkText": "Ex: Windows Server 2016, Ubuntu 16.04 LTS server kernel 4.10.0-14-generic to 4.10.0-32-generic",
            "infoBalloonText": "To find the list of supported Operating System <a href='https://docs.microsoft.com/azure/site-recovery/support-matrix-vmware-to-azure#replicated-machines'>visit here</a>.",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_source_machine_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the host name of the VM (or) failed Job Id:",
            "watermarkText": "Get failed Job Id from (Using new browser tab): Recovery Services Vault - Jobs - Site Recovery Jobs",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "Replication not progressing issues",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "I am trying to Enable Replication for my VM(s), but",
            "watermarkText": "Choose the problem that you are facing",
            "dropdownOptions": [
                {
                    "value": "Replication is stuck at 0%",
                    "text": "Replication is stuck at 0%"
                },
                {
                    "value": "Replication is stuck at 0%",
                    "text": "Replication is stuck at 0%"
                },
                {
                    "value": "VM is protected,but Replication health is critical",
                    "text": "VM is protected, but Replication health is critical"
                },
                {
                    "value": "Application Consistent Snapshot is missing/not latest",
                    "text": "Application Consistent Snapshot is missing/not latest"
                },
                {
                    "value": "My issue is not listed here",
                    "text": "My issue is not listed here"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details:",
            "watermarkText": "Paste error message(s), error code(s) and describe the scenario(s) that are failing.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
