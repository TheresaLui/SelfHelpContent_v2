<properties
                pageTitle="Configuration and Setup"
                description="Configuration and Setup"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32610793"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0081"
	ownershipId="Compute_VirtualMachines"
/>
# Config and Setup
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Create a failover cluster",
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
            "id": "cluster_storage",
            "order": 2,
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
            "id": "quorum_model",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the quorum model in use?",
            "useAsAdditionalDetails": true,
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
