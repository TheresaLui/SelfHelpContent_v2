<properties
	pageTitle="Avere vFXT Cluster Maintenance Activity"
	description="Cluster Maintenance Activity"
	authors="jbut"
	ms.author="jebutl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32609688"
	productPesIds="16506"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="4cae1311-9ee9-4f2d-b92f-18e830048420"
    ownershipId="StorageMediaEdge_AvereVFXT"
/>
# Problems related to cluster maintenance activities.
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Problems related to cluster maintenance activities",
    "formElements": [{
        "id": "avere_cluster_name",
        "order": 1,
        "controlType": "textbox",
        "displayLabel": "Avere vFXT Cluster Name",
        "watermarkText": "Cluster Name",
        "required": true
    }, {
        "id": "avere_os_version",
        "order": 2,
        "controlType": "textbox",
        "displayLabel": "Avere OS Version",
        "watermarkText": "Version Number",
        "required": false
    }, {
        "id": "problem_description",
        "order": 3,
        "controlType": "multilinetextbox",
        "displayLabel": "Description",
        "watermarkText": "Provide additional information about your issue",
        "required": true,
        "useAsAdditionalDetails": true
    }, {
        "id": "problem_start_time",
        "order": 4,
        "controlType": "datetimepicker",
        "displayLabel": "When did the problem start?",
        "required": true
    }]
}
---
