<properties
                pageTitle="VM Performance"
                description="VM Performance"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628270"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0062"
/>
# VM Performance
---
{
    "resourceRequired": true,
    "title": "Guidance for better VM sizing and throughput",
    "fileAttachmentHint": "",
    "formElements": [
    {
        "id": "perf_constraints",
        "order": 1,
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
    },{
            "id": "applications_on_vm",
            "order": 2,
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
        },{
            "id": "perf_storage",
            "order": 3,
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
        },{
				"id": "problem_description",
				"order": 4,
				"controlType": "multilinetextbox",
				"displayLabel": "Description",
				"useAsAdditionalDetails": true,
				"required": true
				}
    ]
}
---
