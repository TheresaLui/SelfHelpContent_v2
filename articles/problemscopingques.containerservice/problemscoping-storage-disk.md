<properties
                pageTitle="Storage/DiskFile Issues"
                description="Storage/DiskFile Issues"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637187"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-storage-disk"
	ownershipId="Compute_AzureKubernetesService"
/>
# Storage/DiskFile Issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Disk/File Issues",
    "fileAttachmentHint": "Attach the output of **kubectl describe pvc 'pvcnamehere'** and **kubectl get pv 'pvcnamehere'**",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "getErrorMsg",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message did you receive while performing this operation, if any?",
            "required": false
        },
        {
            "id": "getVolumeName",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What's the name of underlying volume you have problem with, if any?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
