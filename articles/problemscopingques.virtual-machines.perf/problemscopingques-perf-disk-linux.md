<properties
                pageTitle="VM Performance"
                description="VM Performance"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628264"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0053"
	ownershipId="Compute_VirtualMachines"
/>
# VM Performance
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Disk throughput is lower than expected",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Check for VM disk throttling",
        "description": "We can check your VM for VM disk performance issues.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "disk_throttle_window",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "How many hours back was the disk issue experienced?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "3",
                    "text": "3 hours"
                },
                {
                    "value": "6",
                    "text": "6 hours"
                },
                {
                    "value": "12",
                    "text": "12 hours"
                },
                {
                    "value": "24",
                    "text": "24 hours"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Unknown"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Start time of most recent occurrence",
            "required": true
        },
        {
            "id": "perf_current",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the problem occurring right now?",
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
            "id": "perf_benchmarking",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "Which benchmarking tests have you performed?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "FIO",
                    "text": "FIO"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other (describe below)"
                },
                {
                    "value": "I did not use any",
                    "text": "I did not use any"
                }
            ],
            "required": false
        },
        {
            "id": "applications_on_vm",
            "order": 5,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the applications running on your virtual machine",
            "dropdownOptions": [
                {
                    "value": "Apache Tomcat / Web Front end",
                    "text": "Apache Tomcat / Web Front end"
                },
                {
                    "value": "MongoDB",
                    "text": "MongoDB"
                },
                {
                    "value": "MySQL",
                    "text": "MySQL"
                },
                {
                    "value": "Oracle",
                    "text": "Oracle"
                },
                {
                    "value": "SAP HANA",
                    "text": "SAP HANA"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other (describe below)"
                }
            ],
            "required": false
        },
        {
            "id": "disk_path",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Enter the affected disk path or name",
            "watermarkText": "StorageAccount/Container/DiskName.vhd",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
