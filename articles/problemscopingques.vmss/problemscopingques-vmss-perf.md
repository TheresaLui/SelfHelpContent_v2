<properties
         pageTitle="Performance Issues"
         description="Performance Issues"
         authors="summertgu"
         ms.author="tiag"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32641080"
         productPesIds="16080"
         cloudEnvironments="Public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="b4b6273d-558e-4f2d-ab00-36a830ea0134"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# Performance
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Performance",
    "fileAttachmentHint": "",
    "diagnosticCard": {
            "title": "Virtual machine scale set diagnostics",
            "description": "These diagnostics will check for details about your selected VM instance within your VMSS.",
            "insightNotAvailableText": "We didn't find any problems"},
    "formElements": [
        {
            "id": "vmss_instance",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "If your issue is related to a specific instance, select the instance name",
            "dynamicDropdownOptions": {
                "uri": "{resourceId}/virtualMachines?api-version=2019-03-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to retrieve list of instances.",
                    "text": "Unable to retrieve list of instances."
                }
            ],
            "useAsAdditionalDetails": false,
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problems_scenario_perf",
            "order": 2,
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
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
