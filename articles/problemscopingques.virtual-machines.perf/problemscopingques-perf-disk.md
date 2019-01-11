<properties
                pageTitle="VM Performance"
                description="VM Performance"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628264"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0052"
/>
# VM Performance
---
{
    "resourceRequired": true,
    "title": "Disk throughput is lower than expected",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Start time of most recent occurrence",
            "required": true
        },{
            "id": "perf_current",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the problem current?",
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
        },{
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
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "I did not use any",
                    "text": "I did not use any"
                }
            ],
            "required": false
        },{
						"id": "perf_benchmarking_other",
						"order": 4,
						"visibility": "perf_benchmarking == Other",
						"controlType": "textbox",
						"displayLabel": "Please specify the benchmarking test(s) you performed.",
						"required": false,
						"useAsAdditionalDetails": false
				},{
            "id": "applications_on_vm",
            "order": 5,
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
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Enter the affected disk path or name",
            "watermarkText": "StorageAccount/Container/DiskName.vhd",
            "required": false
        },{
				"id": "problem_description",
				"order": 7,
				"controlType": "multilinetextbox",
				"displayLabel": "Description",
				"useAsAdditionalDetails": true,
				"required": true
				}
    ]
}
---
