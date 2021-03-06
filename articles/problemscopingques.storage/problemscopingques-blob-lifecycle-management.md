<properties
	pageTitle="Blob Lifecycle Management scoping questions"
	description="Blob Lifecycle Management scoping questions"
	authors="broder"
    ms.author="broder"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32683730,32691063"
	productPesIds="16459,16598"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="StorageScoping_Blob_Lifecycle_Management"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>
# Blob Lifecycle Management
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Blob Lifecycle Management Scoping Questions",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Blob Lifecycle Management Troubleshooter",
        "description": "With just a few inputs and a couple of minutes we can help diagnose your problem without the need to open a case.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Please review the recommended solutions below."
    },
    "formElements": [
        {
            "id": "lcm_scenarios",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the scenario that matches your issue",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                    "value": "lcm_did_not_work",
                    "text": "Lifecycle Management did not work at all for this account"
                }, {
                    "value": "lcm_did_not_work_container_blob",
                    "text": "Lifecycle Management did not work for a specific container or blob"
                }, {
                    "text": "Other, my scenario is not listed",
                    "value": "dont_know_answer"
                }
            ],
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "blob_path",
            "order": 2,
            "visibility": "lcm_scenarios == lcm_did_not_work_container_blob",
            "controlType": "textbox",
            "displayLabel": "Provide the container or blob path",
            "watermarkText": "'mycontainer' or 'mycontainer/myblob.txt'",
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate local start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---