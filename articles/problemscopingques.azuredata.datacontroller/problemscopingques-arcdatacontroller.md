<properties
	pageTitle="Azure Arc enabled Data Services"
	description="Azure Arc enabled Data Services"
	ms.author="pradm,amigan"
	selfHelpType="problemScopingQuestions"	supportTopicIds="32743718,32743720,32749972,32749957,32749958,32743716,32743734,32749959,32749960,32749961,32743733,32749962,32743735,32743736,32743717,32743730,32743721,32743727,32743729,32743737,32743728,32749968,32749969,32749970,32749971,32743723,32743725,32743726,32743722,32743724,32743738,32743731,32743732,32743719,32743739,32743740,32749963,32747945,32747946,32747947,32747948,32749964,32749965,32747949,32749966"
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
			"displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Describe your Problem Scenario with relative error messages"
				}, {
					"text": "Platform Version if it is not a native Kubernetes deployment"
				}, {
					"text": "Kubernetes cluster version"
				}, {
					"text": "Kubectl binary version for Kubectl issues"
				}, {
					"text": "azdata version for azdata utility issues"
				}, {
					"text": "Azure Data Studio & Arc Extension version for ADS utility issues"
				}
			]
		}
	]
}
---
