<properties
	pageTitle="Extract information using machine learning models"
	description="Extract information using machine learning models"
	service="microsoft.media"
	resource="mediaservices"
	authors="akucer"
	ms.author="akucer"
	displayOrder="1"
	articleId="mediaservices-lva-extract-information-using-machine-learning"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32740855"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>
# Extract information using machine learning models
## **Recommended Steps**
Live Video Analytics on IoT Edge is designed to be a pluggable platform, enabling you to plug video analysis edge modules (for example, Cognitive services containers, custom edge modules built by you with open-source machine learning models or custom models trained with your own data) and use them to analyze live video without worrying about the complexity of building and running a live video pipeline.

Follow the [Quickstart: Analyze live video with your own model](https://docs.microsoft.com/azure/media-services/live-video-analytics-edge/use-your-model-quickstart) for details on applying computer vision to analyze live videos. You will be able to filter a subset of the video frames, convert them to images and send them to an inference module that applies computer vision to detect objects in those images. The events returned by the inference module will be published to IoT Edge Hub.

