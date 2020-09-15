<properties
	pageTitle="Azure Arc enabled Data Services"
	description="Azure Arc enabled Data Services"
	ms.author="pradm,amigan"
	selfHelpType="problemScopingQuestions"	supportTopicIds="32743716,32743717,32743734,32743735,32743733,32743736,32743721,32743727,32743728,32743729,32743730,32743737,32743725,32743726,32743722,32743723,32743724,32743738,32747945,32747946,32747947,32747948,32747949,32743719,32743731,32743732,32743739,32743740,32743718,32743720"
	productPesIds="17076"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="818f3de8-43de-48ac-89d5-9bdd5ac7134b"
	ownershipId="AzureData_SQL_Azure_Hybrid_Data_Platform"
/>
# Azure Arc enabled Data Services
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Azure Arc enabled Data Services",
	"fileAttachmentHint": "",
	"formElements": [
		{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "kubernetes_cluster_cloud",
			"order": 2,
			"controlType": "dropdown",
			"infoBalloonText": "string",
			"displayLabel": "Is the Kubernetes cluster on Cloud?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "cloud_kubernetes",
			"order": 3,
			"visibility": "kubernetes_cluster_cloud == Yes",
			"controlType": "dropdown",
			"displayLabel": "Which is your Cloud Kubernetes Platform?",
			"dropdownOptions": [{
					"value": "AKS",
					"text": "Azure Kubernetes Service (AKS)"
				}, {
					"value": "ARO",
					"text": "Azure RedHat OpenShift (ARO)"
				}, {
					"value": "GKE",
					"text": "Google Kubernetes Engine (GKE)"
				}, {
					"value": "EKS",
					"text": "AWS Elastic Kubernetes Service (EKS)"
				}, {
					"value": "OpenShift 4.2+",
					"text": "OpenShift Container Platform (OCP) 4.2+ on Cloud VMs"
				}, {
					"value": "Native Kubernetes",
					"text": "Native Kubernetes 1.14+ on Cloud VMs"
				}, {
					"value": "Other",
					"text": "Other"
				}, {
					"value": "more_info",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": false
		}, {
			"id": "onprem_kubernetes",
			"order": 4,
			"visibility": "kubernetes_cluster_cloud == No",
			"controlType": "dropdown",
			"displayLabel": "Which is your on-premise Kubernetes Platform?",
			"dropdownOptions": [{
					"value": "Native Kubernetes 1.14+",
					"text": "Native Kubernetes 1.14+"
				}, {
					"value": "OpenShift Container Platform (OCP) 4.2+",
					"text": "OpenShift Container Platform (OCP) 4.2+"
				}, {
					"value": "Azure Kubernetes Engine (AKE) on Azure Stack",
					"text": "Azure Kubernetes Engine (AKE) on Azure Stack"
				}, {
					"value": "more_info",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": false
		}, {
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Describe your Problem Scenario, with the relative error messages if any. Also share these details along with the scenario, if possible."
				}, {
					"text": " a. Platform Version if it is not a Native Kubernetes deployment"
				}, {
					"text": " b. Kubernetes cluster version"
				}, {
					"text": " c. Kubectl binary version if the issue involves using Kubectl utility"
				}, {
					"text": " d. azdata version if the issue involves using azdata utility"
				}, {
					"text": " e. Azure Data Studio version & Data Controller Extension version if the issue involves using ADS utility"
				}
			]
		}
	]
}
---
