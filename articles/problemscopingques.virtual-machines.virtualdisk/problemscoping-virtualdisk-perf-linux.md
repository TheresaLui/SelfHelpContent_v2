<properties
                pageTitle="Virtual Disk Management"
                description="Virtual Disk Management"
                authors="summertgu,timbasham"
                ms.author="tiag,tibasham"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32640592"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="c7ba78fb-a44c-4cec-b332-7fb4cc5d583f"
	ownershipId="Compute_VirtualMachines"
/>
# Virtual Disk Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Disk throughput is lower than expected",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Start time of most recent occurrence",
            "required": true
        },
        {
            "id": "perf_current",
            "order": 2,
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
            "order": 3,
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
            "order": 4,
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
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Enter the affected disk path or name",
            "watermarkText": "StorageAccount/Container/DiskName.vhd",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
