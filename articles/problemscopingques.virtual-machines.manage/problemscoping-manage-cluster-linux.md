<properties
                pageTitle="Management"
                description="Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32411818"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0086"
	ownershipId="Compute_VirtualMachines"
/>
# Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Manage or use a cluster in Azure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "manage_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "cluster_operation",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What operation are you trying to do?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Add a cluster",
                    "text": "Add a cluster"
                },
                {
                    "value": "Remove a cluster",
                    "text": "Remove a cluster"
                },
                {
                    "value": "Start a cluster",
                    "text": "Start a cluster"
                },
                {
                    "value": "Scale a cluster",
                    "text": "Scale a cluster"
                },
                {
                    "value": "Troubleshoot a cluster",
                    "text": "Troubleshoot a cluster"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "cluster_storage",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What storage are you using?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "iSCSI",
                    "text": "iSCSI"
                },
                {
                    "value": "NFS",
                    "text": "NFS"
                },
                {
                    "value": "SMB",
                    "text": "SMB"
                }
            ],
            "required": false
        },
        {
            "id": "node_number",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "How many nodes are there in the cluster?",
            "required": false
        },
        {
            "id": "node_subnet",
            "order": 5,
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
            "id": "quorum_model",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the quorum model in use?",
            "useAsAdditionalDetails": false,
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
