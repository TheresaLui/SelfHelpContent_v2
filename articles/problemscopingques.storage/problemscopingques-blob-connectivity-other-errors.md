<properties
	pageTitle="Blob connectivity other blob service errors"
	description="Blob connectivity and other blob service errors scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602728"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Blob connectivity other blob service errors
---
{
	"resourceRequired": true,
	"title": "Blob connectivity other blob service errors scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Approximate local start time of the latest occurrence",
			"required": true
		}, {
			"id": "error_code_dropdown",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Error code",
			"watermarkText": "HTTP error of failed operation",
			"dropdownOptions": [{
					"value": "HTTP_304",
					"text": "HTTP 304"
				}, {
					"value": "HTTP_400",
					"text": "HTTP 400"
				}, {
					"value": "HTTP_403",
					"text": "HTTP 403"
				}, {
					"value": "HTTP_404",
					"text": "HTTP 404"
				}, {
					"value": "HTTP_405",
					"text": "HTTP 405"
				}, {
					"value": "HTTP_409",
					"text": "HTTP 409"
				}, {
					"value": "HTTP_411",
					"text": "HTTP 411"
				}, {
					"value": "HTTP_412",
					"text": "HTTP 412"
				}, {
					"value": "HTTP_413",
					"text": "HTTP 413"
				}, {
					"value": "HTTP_415",
					"text": "HTTP 415"
				}, {
					"value": "HTTP_416",
					"text": "HTTP 416"
				}, {
					"value": "HTTP_500",
					"text": "HTTP 500"
				}, {
					"value": "HTTP_501",
					"text": "HTTP 501"
				}, {
					"value": "HTTP_502",
					"text": "HTTP 502"
				}, {
					"value": "HTTP_503",
					"text": "HTTP 503"
				}, {
					"value": "other",
					"text": "Not listed above  "
				}
			],
			"required": false
		}, {
			"id": "request_id",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Storage server Request ID",
			"watermarkText": "Request ID of failed operation",
			"required": false
		}, {
			"id": "blob_or_container",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Container name or Blob path",
			"watermarkText": "'ContainerName' or 'ContainerName/../BlobName' if specific to a container or blob",
			"required": false
		}, {
			"id": "additional_details",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true
		}
	]
}
---
