<properties
                pageTitle="Management"
                description="Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32411819"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0093"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Manage or use RDS in Azure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "opreation_rds",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What are you trying to do?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Create the RDS",
                    "text": "Create the RDS"
                },
                {
                    "value": "Configure the RDS",
                    "text": "Configure the RDS"
                },
                {
                    "value": "Manage the RDS",
                    "text": "Manage the RDS"
                }
            ],
            "required": false
        },
        {
            "id": "number_license",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "How many licenses are you trying to configure?",
            "required": false
        },
        {
            "id": "all_user_impacted",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are all users impacted?",
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
            "id": "if_performance",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is this a performance issue?",
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
            "id": "upd_store",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Where would the UPD be stored?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "This local machine",
                    "text": "This local machine"
                },
                {
                    "value": "Configured remotely",
                    "text": "Configured remotely"
                }
            ],
            "required": false
        },
        {
            "id": "app_cluster",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Are there any other application or clusters configured on this server?",
            "useAsAdditionalDetails": true,
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
