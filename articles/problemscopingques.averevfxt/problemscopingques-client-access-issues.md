<properties
	pageTitle="Avere vFXT Client Access Issues"
	description="Client Access Issues"
	authors="jbut"
	ms.author="jebutl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32609686"
	productPesIds="16506"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="b57b5e5d-94b5-498e-93e1-a5fa74e8cdee"
    ownershipId="StorageMediaEdge_AvereVFXT"
/>
# Problems with client access to Avere vFXT cluster.
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Problems with client access to Avere vFXT cluster",
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
        "id": "avere_client_name_or_ip",
        "order": 3,
        "controlType": "textbox",
        "displayLabel": "Client Name or IP Address",
        "watermarkText": "Name or IP Address",
        "required": false
    }, {
        "id": "problem_description",
        "order": 4,
        "controlType": "multilinetextbox",
        "displayLabel": "Description",
        "watermarkText": "Provide additional information about your issue",
        "required": true,
        "useAsAdditionalDetails": true
    }, {
        "id": "problem_start_time",
        "order": 5,
        "controlType": "datetimepicker",
        "displayLabel": "When did the problem start?",
        "required": true
    }]
}
---
