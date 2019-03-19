{
 "resourceRequired": true,
 "title": "Intermittent connectivity issues",
 "fileAttachmentHint": "",
 "formElements": [
	 {
	 "id": "connectivity_direction"
	 "order": 1,
	 "controlType": "dropdown",
	 "displayLabel": "Please specify the connectivity direction",
	 "watermarkText": "Choose an option",
	 "dropdownOptions": [
		 {
		 "value": "Inbound to the backend pool",
		 "text": "Inbound to the backend pool"
		 },
		 {
		 "value": "Outbound from the backend pool",
		 "text": "Outbound from the backend pool"
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
			 "text": "Source / Destination details (e.f. IP Address, URL)"
			 },
			 {
			 "text": "Did the connectivity work in the past and stopped working now?"
			 },
			 {
			 "text": "Does the direct access to / from the backend pool instances (without the load balancer IP Address) work?"
			 },
			 {
			 "text": "Did you recieve any error messages from the Load Balancer that you want to share?"
			 }
		] }
 ] 
}