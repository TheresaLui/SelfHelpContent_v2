<properties
    pageTitle="Media Services LiveEvent errors"
    description="Media Services LiveEvent errors"
    authors="johndeu"
    ms.author="johndeu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32632071,32632083, 32632105, 32632108, 32632120"
    productPesIds="14885"
    articleId="problemscopingques-liveevent-errors"
    cloudEnvironments="public"
    schemaVersion="1"
/>
# Media Services Live Event or Channel connectivity or encoding errors
---
{
    "resourceRequired": true,
    "title": "Live Event or Channel connectivity or encoding errors",
    "fileAttachmentHint": "On-premises live encoder log files, Encoding configuration preset settings, or NetMon, Wireshark, or Fiddler network trace of issue (if available)",
    "formElements": [{
            "id": "liveEvent_Errors",
            "order": 1,
            "controlType": "dropdown",
            "infoBalloonText": "See overview of types of LiveEvents available in the article <a href='https://docs.microsoft.com/azure/media-services/latest/live-streaming-overview#live-event-types'>live event types overview</a>",
            "displayLabel": "Are you using a pass-through or cloud encoding LiveEvent/Channel?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                "value": "pass-through",
                "text": "pass-through"
            }, {
                "value": "live-encoding",
                "text": "live encoding"
            }, {
                "value": "dont_know_answer",
                "text": "Don't Know"
            }],
            "required": true
        }, {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When time did the LiveEvent/Channel start or problem occur?",
            "required": true
        },
        {
            "id": "liveEvent_protocol",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which live ingest protocol are you using?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                "value": "RTMP",
                "text": "RTMP"
            }, {
                "value": "Fragmented MP4 (Smooth)",
                "text": "Fragmented MP4 (Smooth)"
            }, {
                "value": "dont_know_answer",
                "text": "Don't Know"
            }],
            "required": true
        },
        {
            "id": "live_encoder_type",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Which recommmended on-premises live encoders for Media Services are you using? See <a href='https://go.microsoft.com/fwlink/?linkid=2087173'> recommended encoders </a>",
            "dropdownOptions": [{
                "value": "Adobe Flash Media Live Encoder 3.2",
                "text": "Adobe Flash Media Live Encoder 3.2+"
            }, {
                "value": "Ateme TITAN Live",
                "text": "Ateme TITAN Live"
            }, {
                "value": "Cisco Digital Media Encoder 2200",
                "text": "Cisco Digital Media Encoder 2200"
            }, {
                "value": "Elemental Live",
                "text": "Elemental Live"
            }, {
                "value": "FFMpeg",
                "text": "FFMpeg v4+"
            }, {
                "value": "Envivio 4Caster C4 Gen III",
                "text": "Envivio 4Caster C4 Gen III"
            }, {
                "value": "Haivision KB",
                "text": "Haivision KB"
            }, {
                "value": "Haivision Makito X HEVC",
                "text": "Haivision Makito X HEVC"
            }, {
                "value": "Imagine Communications Selenio",
                "text": "Imagine Communications Selenio"
            }, {
                "value": "Media Excel Hero Live and Hero 4K (UHD/HEVC)",
                "text": "Media Excel Hero Live and Hero 4K (UHD/HEVC)"
            }, {
                "value": "OBS Studio",
                "text": "OBS Studio"
            }, {
                "value": "Switcher Studio (iOS)",
                "text": "Switcher Studio (iOS)"
            }, {
                "value": "Telestream Wirecast 8.1+",
                "text": "Telestream Wirecast 8.1+"
            }, {
                "value": "Telestream Wirecast S",
                "text": "Telestream Wirecast S"
            }, {
                "value": "Teradek Slice 756",
                "text": "Teradek Slice 756"
            }, {
                "value": "TriCaster 8000",
                "text": "TriCaster 8000"
            }, {
                "value": "Tricaster Mini HD-4",
                "text": "Tricaster Mini HD-4"
            }, {
                "value": "VMIX",
                "text": "VMIX"
            }, {
                "value": "xStream",
                "text": "xStream"
            }, {
                "value": "Other (unsupported encoder)",
                "text": "Other (not using one of the recommended encoders above)"
            }],
            "required": true
        },
        {
            "id": "ffmpeg_command",
            "order": 5,
            "visibility": "live_encoder_type == FFMpeg",
            "controlType": "multilinetextbox",
            "displayLabel": "FFMpeg Command Line used",
            "watermarkText": "Provide the exact FFMpeg command line that you are using",
            "required": false,
            "useAsAdditionalDetails": false,
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your Live Event broadcast configuration settings or on-premises encoder",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [{
                "text": "Issue description."
            }, {
                "text": "Provide details about the setup of your Live Event, Encoder configuration settings, etc. Please upload your encoder settings file if that is also available."
            }]
        }, {
            "id": "learn_more_text",
            "order": 7,
            "controlType": "infoblock",
            "content": "See more details about <a href='https://go.microsoft.com/fwlink/?linkid=2087173'>recommended live encoders</a> in the documentation."
        }
    ]
}
---