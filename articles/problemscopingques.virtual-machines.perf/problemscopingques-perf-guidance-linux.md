<properties
                pageTitle="VM Performance"
                description="VM Performance"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628270"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0063"
	ownershipId="Compute_VirtualMachines"
/>
# VM Performance
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Guidance for better VM sizing and throughput",
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
            "id": "perf_constraints",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "Which category of resource constraints did you observe?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "CPU",
                    "text": "CPU"
                },
                {
                    "value": "Memory",
                    "text": "Memory"
                },
                {
                    "value": "Disk",
                    "text": "Disk"
                },
                {
                    "value": "Network",
                    "text": "Network"
                },
                {
                    "value": "GPU",
                    "text": "GPU"
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
            "id": "perf_storage",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Are your VMs using Standard Storage or Premium Storage?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Standard Storage",
                    "text": "Standard Storage"
                },
                {
                    "value": "Premium Storage",
                    "text": "Premium Storage"
                }
            ],
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
