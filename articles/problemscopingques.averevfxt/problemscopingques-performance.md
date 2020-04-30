<properties
	pageTitle="Avere vFXT Performance Issues"
	description="Performance Issues"
	authors="jbut"
	ms.author="jebutl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32609694"
	productPesIds="16506"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="6a0f54a0-705c-4cc9-a28f-bf43e5a3611c"
    ownershipId="StorageMediaEdge_AvereVFXT"
/>
# Performance Issues
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Performance Issues",
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
        "id": "avere_expected_performance",
        "order": 3,
        "controlType": "multilinetextbox",
        "displayLabel": "Expected Performance",
        "watermarkText": "Describe expected performance",
        "required": false,
        "useAsAdditionalDetails": false
    }, {
        "id": "avere_env_changes",
        "order": 4,
        "controlType": "multilinetextbox",
        "displayLabel": "Changes to Deployment",
        "watermarkText": "Describe any recent changes that you made to your deployment or environment that may be responsible for the performance issues.",
        "required": false,
        "useAsAdditionalDetails": false
    }, {
        "id": "problem_description",
        "order": 5,
        "controlType": "multilinetextbox",
        "displayLabel": "Description",
        "watermarkText": "Provide additional information about your issue",
        "required": true,
        "useAsAdditionalDetails": true
    }, {
        "id": "problem_start_time",
        "order": 6,
        "controlType": "datetimepicker",
        "displayLabel": "When did the problem start?",
        "required": true
    }]
}
---
