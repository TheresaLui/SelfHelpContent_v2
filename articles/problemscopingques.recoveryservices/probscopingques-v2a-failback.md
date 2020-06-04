<properties
         pageTitle="Scoping questions for Failback from Azure to on-premises VMware"
         description="Scoping questions for Failback from Azure to on-premises VMware"
         authors="ashishgangwar"
	     ms.author="asgang, TobyTu"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32536408"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	     articleId="666ae305-e3c9-4c5c-89d5-febc5ce66b79"
	ownershipId="Compute_SiteRecovery"
/>
# Failback from Azure to on-premises VMware
---
{
    "$schema": "SelfHelpContent",
     "subscriptionRequired": true,
     "resourceRequired": true,
    "title": "failback from Azure to on-premises",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide name of the VM being failed back from Azure to on-premises",
            "watermarkText": "Enter name(s) to scope down quickly",
            "required": true
        },
        {
            "id": "error_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide error ID or job ID of the failback operation",
            "watermarkText": "Enter in the error or job ID",
            "infoBalloonText": "Open a new tab, navigate to Recovery Services Vault, click on Jobs & paste error or job ID of failed failback job",
            "required": false
        },
        {
            "id": "trouble_action",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "I am trying to failback, but",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "My re-protect job has failed",
                    "text": "My re-protect job has failed"
                },
                {
                    "value": "I am unable to connect from Azure to on-premises",
                    "text": "I am unable to connect from Azure to on-premises"
                },
                {
                    "value": "I am unable to set up process server in Azure",
                    "text": "I am unable to set up process server in Azure"
                },
                {
                    "value": "I am not able to boot or see all disks after failback",
                    "text": "I am not able to boot or see all disks after failback"
                },
                {
                    "value": "My original vCenter is not available",
                    "text": "My original vCenter is not available"
                },
                {
                    "value": "My original configuration server is not available",
                    "text": "My original configuration server is not available"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "tried_steps",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "I have gone through steps provided in the following articles",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Failback of VMware VMs after disaster recovery to Azure",
                    "text": "Failback of VMware VMs after disaster recovery to Azure"
                },
                {
                    "value": "Troubleshoot failback to on-premises from Azure",
                    "text": "Troubleshoot failback to on-premises from Azure"
                },
                {
                    "value": "Set up a process server in Azure for failback",
                    "text": "Set up a process server in Azure for failback"
                },
                {
                    "value": "Fail back VMware VMs and physical servers from Azure",
                    "text": "Fail back VMware VMs and physical servers from Azure"
                },
                {
                    "value": "Install a Linux master target server for failback",
                    "text": "Install a Linux master target server for failback"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
       {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "watermarkText": "Enter in local time",
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