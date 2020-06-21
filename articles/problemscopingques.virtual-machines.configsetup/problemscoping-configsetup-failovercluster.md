<properties
                pageTitle="Configuration and Setup"
                description="Configuration and Setup"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32411853"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0082"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Config and Setup
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Create a Windows failover cluster",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "cluster_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What is the cluster name?",
            "required": false
        },
        {
            "id": "is_s2d",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is this a Storage Spaced Direct Cluster(S2D)?",
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
            "id": "node_number",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "How many nodes are there in the cluster?",
            "required": false
        },
        {
            "id": "node_subnet",
            "order": 4,
            "visibility": "node_number != 1",
            "controlType": "dropdown",
            "displayLabel": "Are the nodes in the same or different subnets?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "role_cluster",
            "order": 5,
            "controlType": "multiselectdropdown",
            "displayLabel": "What is/are the role/roles running on the cluster?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Hyper-V",
                    "text": "Hyper-V"
                },
                {
                    "value": "File share",
                    "text": "File share"
                },
                {
                    "value": "Exchange",
                    "text": "Exchange"
                },
                {
                    "value": "SQL Server",
                    "text": "SQL Server"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "quorum_model",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the quorum model in use?",
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
