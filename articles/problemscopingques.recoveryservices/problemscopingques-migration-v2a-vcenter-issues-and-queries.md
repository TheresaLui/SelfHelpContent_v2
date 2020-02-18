<properties
         pageTitle="Scoping questions for vCenter issues and queries  "
         description="Scoping questions for vCenter issues and queries"
         authors="ashishgangwar, TobyTu"
         ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32680624"
         productPesIds="16370"
         cloudEnvironments="public"
         schemaVersion="1"
         articleId="8b342a85-0813-4b4d-b7d0-43639892e013"
/>

# Questions for vCenter issues and queries

---
{
    "$schema": "SelfHelpContent",
     "subscriptionRequired": true,
     "resourceRequired": true,
    "title": "vCenter issues and queries",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vcenter_version",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What is the version of vCenter?",
            "watermarkText": "Ex: vSphere client 5.5 or ESXi host 6.0",
            "required": true
        },
        {
            "id": "error_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide error ID associated to vCenter seen on the Azure portal",
            "watermarkText": "Enter in the error ID",
            "infoBalloonText": "Open a new tab, navigate to Recovery Services Vault, paste the error code seen for vCenter in the overview blade",
            "required": false
        },
        {
            "id": "trouble_action",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Choose the action you are having trouble with",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Upgrade my existing vCenter to the latest version",
                    "text": "Upgrade my existing vCenter to the latest version"
                },
                {
                    "value": "My existing vCenter is not connected",
                    "text": "My existing vCenter is not connected"
                },
                {
                    "value": "Add a new vCenter to a same vault",
                    "text": "Add a new vCenter to a same vault"
                },
                {
                    "value": "Move few VMs to a new vCenter",
                    "text": "Move few VMs to a new vCenter"
                },
                {
                    "value": "Unable to see VMs under the existing vCenter",
                    "text": "Unable to see VMs under the existing vCenter"
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
                    "value": "ASR manage VMware vCenter server",
                    "text": "ASR manage VMware vCenter server"
                },
                {
                    "value": "Prepare on-premises VMware servers",
                    "text": "Prepare on-premises VMware servers"
                },
                {
                    "value": "Common questions about VMware to Azure replication",
                    "text": "Common questions about VMware to Azure replication"
                },
                {
                    "value": "Troubleshoot vCenter discovery failures",
                    "text": "Troubleshoot vCenter discovery failures"
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
