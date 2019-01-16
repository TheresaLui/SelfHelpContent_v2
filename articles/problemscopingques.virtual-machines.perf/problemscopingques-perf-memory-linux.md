<properties
                pageTitle="VM Performance"
                description="VM Performance"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628275"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0059"
/>
# VM Performance
---
{
    "resourceRequired": true,
    "title": "Memory usage is higher than expected",
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
        },{
            "id": "perf_memory_detect",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "How did you detect high memory usage?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Monitoring Alerts",
                    "text": "Azure Monitoring Alerts"
                },
                {
                    "value": "Other Monitoring tools (describe below)",
                    "text": "Other Monitoring tools (describe below)"
                }
            ],
            "required": false
        },{
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
  				"id": "perf_memory_apps",
  				"order": 5,
  				"controlType": "multilinetextbox",
  				"displayLabel": "List all processes/applications you have identified that cause the high memory usage.",
  				"useAsAdditionalDetails": false,
  				"required": true
				},{
				"id": "problem_description",
				"order": 6,
				"controlType": "multilinetextbox",
				"displayLabel": "Description",
				"useAsAdditionalDetails": true,
				"required": true
				}
    ]
}
---
