<properties
         pageTitle="Virtual Machine running Citrix"
         description="Virtual Machine running Citrix"
         authors="summertgu"
         ms.author="tiag"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32567272, 32567277, 32567281, 32567286"
         productPesIds="16215"
         cloudEnvironments="Public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="b4b6273d-558e-4f2d-ab00-36a830ea69"
	ownershipId="Compute_VirtualMachines"
/>
# Citrix VM Connectivity
---
{
                "subscriptionRequired": true,
                "resourceRequired": false,
                "title": "Performance",
                "fileAttachmentHint": "",
                "formElements": [
        {
            "id": "problems_scenario_perf",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please specify your issue.",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Disk throughput is lower than expected",
                    "text": "Disk throughput is lower than expected"
                },
                {
                    "value": "CPU usage is higher than expected",
                    "text": "CPU usage is higher than expected"
                },
                {
                    "value": "Network throughput is slower than expected",
                    "text": "Network throughput is slower than expected"
                },
                {
                    "value": "Memory usage is higher than expected",
                    "text": "Memory usage is higher than expected"
                },
                {
                    "value": "GPU processing is slower than expected",
                    "text": "GPU processing is slower than expected"
                },
                {
                    "value": "Guidance for better VM sizing and throughput",
                    "text": "Guidance for better VM sizing and throughput"
                },
                {
                    "value": "Replication of Shared Image Version is slow",
                    "text": "Replication of Shared Image Version is slow"
                },
                {
                    "value": "Backup",
                    "text": "Backup"
                },
                {
                    "value": "Write Accelerator",
                    "text": "Write Accelerator"
                }
            ],
            "required": false
        },
        {
            "id": "citrixcase",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Do you have a support case with Citrix?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "citrixcase_id",
            "order": 3,
            "visibility": "citrixcase == Yes",
            "controlType": "textbox",
            "displayLabel": "Citrix support case number",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
