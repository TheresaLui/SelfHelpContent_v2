{
 "resourceRequired": true,
 "title": "Configure Load Balancer Telemetry",
 "fileAttachmentHint": "",
 "formElements": [	 
	 {
	 "id": "config_lb_sku"
	 "order": 1,
	 "controlType": "dropdown",
	 "displayLabel": "Please select the Load Balancer resource type that you need help with",
	 "watermarkText": "Choose an option",
	 "dropdownOptions": [
		 {
		 "value": "Basic SKU",
		 "text": "Basic SKU"
		 },
		 {
		 "value": "Standard SKU",
		 "text": "Standard SKU"
		 },
	 ],
	 "required": true
	 },
	 {
	 "id": "config_lb_type"
	 "order": 2,
	 "controlType": "dropdown",
	 "displayLabel": "Please select the Load Balancer resource type that you need help with",
	 "watermarkText": "Choose an option",
	 "dropdownOptions": [
		 {
		 "value": "Internal Load Balancer",
		 "text": "Internal Load Balancer"
		 },
		 {
		 "value": "Public Load Balancer",
		 "text": "Public Load Balancer"
		 },
	 ],
	 "required": true
	 },
	 {
	 "id": "config_temetry_type"
	 "order": 3,
	 "controlType": "dropdown",
	 "displayLabel": "Please select the telemetry category that you need help with",
	 "watermarkText": "Choose an option",
	 "dropdownOptions": [
		 {
		 "value": "Log Analytics",
		 "text": "Log Analytics"
		 },
		 {
		 "value": "Multi-Dimensional Metrics",
		 "text": "Multi-Dimensional Metrics"
		 },
		 {
		 "value": "Resource Health",
		 "text": "Resource Health"
		 },
		 {
		 "value": "Alerts",
		 "text": "Alerts"
		 },
	 ],
	 "required": true
	 },
	 {
		 "id": "problem_start_time",
		 "order": 4,
		 "controlType": "datetimepicker",
		 "displayLabel": "When did the problem begin?",
		 "required": false
	 },
	 {
		 "id": "problem_description",
		 "order": 5,
		 "controlType": "multilinetextbox",
		 "displayLabel": "Please specify any additional details or questions",
		 "required": false, 
		 "useAsAdditionalDetails": true,
		 "hints": [
			 {
			 "text": "Did you recieve any error messages while configuring Load Balancer telemetry? (If yes, please share the error message as well)"
			 }
		] }
 ] 
}