<properties
                pageTitle="Virtual Disk Management"
                description="Virtual Disk Management"
                authors="summertgu,timbasham"
                ms.author="tiag,tibasham"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32640592"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="e01786ed-f6e2-4846-8594-f51f4719c5f9"
	ownershipId="Compute_VirtualMachines_Content"
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
                    "value": "Perf Insights",
                    "text": "Perf Insights"
                },
                {
                    "value": "DiskSPD",
                    "text": "DiskSPD"
                },
                {
                    "value": "IOmeter",
                    "text": "IOmeter"
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
                    "value": "CRM Dynamics",
                    "text": "CRM Dynamics"
                },
                {
                    "value": "IIS / Web Front end",
                    "text": "IIS / Web Front end"
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
                    "value": "Remote Desktop Services",
                    "text": "Remote Desktop Services"
                },
                {
                    "value": "SAP HANA",
                    "text": "SAP HANA"
                },
                {
                    "value": "SharePoint",
                    "text": "SharePoint"
                },
                {
                    "value": "SQL",
                    "text": "SQL"
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
