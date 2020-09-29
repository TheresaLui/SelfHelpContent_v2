<properties
         pageTitle="Scoping questions for Vmware to Azure enable replication"
         description="Scoping questions for Vmware to Azure enable replication"
         authors="Rajeswarimamilla"
         ms.author="aaronmax"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32680607"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="7fd2dd45-a2cc-4a69-9e92-57c45dafa5b8"
	ownershipId="Compute_SiteRecovery"
/>
# Questions Azure site recovery - Vmware to Azure Enable replication
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Site recovery enable replication failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "os_version",
            "order": 1,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "What is the OS version of the impacted Server?",
            "watermarkText": "Ex: Windows Server 2016, Ubuntu 16.04 LTS server kernel 4.10.0-14-generic to 4.10.0-32-generic",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "learn_more_text_1",
            "order": 3,
            "visibility": "null",
            "controlType": "infoblock",
            "content": "To find the list of supported Operating System <a href='https://docs.microsoft.com/azure/site-recovery/support-matrix-vmware-to-azure#replicated-machines'>visit here</a>."
        },
        {
            "id": "problem_source_machine_name",
            "order": 4,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the host name of the VM",
            "watermarkText": "Get failed Job Id from (Using new browser tab): Recovery Services Vault -- Jobs -- Site Recovery Jobs",
            "required": false
        },
        {
            "id": "issue_Type",
            "visibility": "null",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "I am trying to Enable replication, but",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Push installation failed due to connectivity errors",
                    "text": "Push installation failed due to connectivity errors"
                },
                {
                    "value": "Push installation failed due to unsupported version",
                    "text": "Push installation failure due to unsupported version"
                },
                {
                    "value": "Push installation failed due to boot/disc/root configurations",
                    "text": "Push installation failed due to boot/disc/root configurations"
                },
                {
                    "value": "Push installation succeeded but VSS installation failed",
                    "text": "Push installation succeeded but VSS installation failed"
                },
                {
                    "value": "Failed to register configuration server with my source machine",
                    "text": "Failed to register configuration server with my source machine"
                },
                {
                    "value": "Passphrase/invalid IP error",
                    "text": "Passphrase/invalid IP error"
                },
                {
                    "value": "Configuration server is not connected",
                    "text": "Configuration server is not connected"
                },
                {
                    "value": "My initial replication is stuck",
                    "text": "My initial replication is stuck"
                },
                {
                    "value": "My issue isn't listed here",
                    "text": "My issue isn't listed here"
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
            "order": 6,
            "controlType": "multiselectdropdown",
            "displayLabel": "I have gone through following steps:",
            "dropdownOptions": [
                {
                    "value": "Credentials used are correct and have admin privileges",
                    "text": "Credentials used are correct and have admin privileges"
                },
                {
                    "value": "VM has required connectivity",
                    "text": "VM has required connectivity"
                },
                {
                    "value": "VM OS/kernel/boot/root/disk configurations are supported",
                    "text": "VM OS/kernel/boot/root/disk configurations are supported"
                },
                {
                    "value": "Manually installed Azure Site Recovery VSS provider",
                    "text": "Manually installed Azure Site Recovery VSS provider"
                },
                {
                    "value": "Other, don't know or not applicable",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "learn_more_text1",
            "order": 7,
            "visibility": "issue_Type == Push installation failed due to connectivity errors",
            "controlType": "infoblock",
            "content": "Most of the Push installation issues get resolved using our troubleshooting article, Try these <a href='https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install'> troubleshooting steps</a> to self-resolve the issue."
        },
        {
            "id": "learn_more_text2",
            "order": 8,
            "visibility": "issue_Type == Push installation failure due to unsupported version",
            "controlType": "infoblock",
            "content": "Ensure source machine has the <a href='https://docs.microsoft.com/azure/site-recovery/support-matrix-vmware-to-azure#replicated-machines'> supported Operating System/Kernel version</a> for successful installation of Mobility service."
        },
        {
            "id": "learn_more_text3",
            "order": 9,
            "visibility": "issue_Type == My initial replication is stuck",
            "controlType": "infoblock",
            "content": "Most of the initial replication issues get resolved using our troubleshooting article, Try these <a href='https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#initial-replication-issues'> troubleshooting steps</a> to self-resolve the issue."
        },
        {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---
