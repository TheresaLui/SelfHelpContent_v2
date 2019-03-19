<properties
	pageTitle="No connectivity to the backend pool"
	description="No connectivity to the backend pool"
	authors="rdhillon"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588977"
	productPesIds="16098"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId=""
/>
# SLB - No connectivity to the backend pool
---
{
 "resourceRequired": true,
 "title": "No connectivity to the backend pool",
 "fileAttachmentHint": "",
 "formElements": [
	 {
	 "id": "inbound-connectivity"
	 "order": 1,
	 "controlType": "dropdown",
	 "displayLabel": "Please specify the source location",
	 "watermarkText": "Choose an option",
	 "dropdownOptions": [
		 {
		 "value": "Within virtual network",
		 "text": "Within virtual network"
		 },
		 {
		 "value": "A peered virtual network in the same region",
		 "text": "A peered virtual network in the same region"
		 },
		 {
		 "value": "A peered virtual network in a different region",
		 "text": "A peered virtual network in a different region"
		 },
		 {
		 "value": "External Internet endpoint",
		 "text": "External Internet endpoint"
		 },
	 ],
	 "required": true
	 },
	 {
	 "id": "connectivity-break-type"
	 "order": 2,
	 "controlType": "dropdown",
	 "displayLabel": "Please specify the type of connectivity loss",
	 "watermarkText": "Choose an option",
	 "dropdownOptions": [
		 {
		 "value": "Intermittent connectivity loss",
		 "text": "Intermittent connectivity loss"
		 },
		 {
		 "value": "Persistent problem",
		 "text": "Persistent problem"
		 }
	 ],
	 "required": true
	 },	 
	 {
		 "id": "problem_start_time",
		 "order": 3,
		 "controlType": "datetimepicker",
		 "displayLabel": "When did the problem begin?",
		 "required": true
	 },
	 {
		 "id": "problem_description",
		 "order": 5,
		 "controlType": "multilinetextbox",
		 "displayLabel": "Please specify any additional details",
		 "required": false, 
		 "useAsAdditionalDetails": true,
		 "hints": [
			 {
			 "text": "Source details (e.f. IP Address)"
			 },
			 {
			 "text": "Did the connectivity work in the past and stopped working now?"
			 },
			 {
			 "text": "Can you access the backend pool instances directly without the load balancer?"
			 },
			 {
			 "text": "Did you recieve any error messages from the Load Balancer that you want to share?"
			 }
		] }
 ] 
}
---
