<properties
	pageTitle="Problem using custom Docker images or Dockerfile"
	description="Problem using custom Docker images or Dockerfile"
	infoBubbleText="Problem using custom Docker images or Dockerfile"
	service="microsoft.machinelearning"
	resource="environments"
	authors="saachigopal"
	ms.author="sagopal"
	supportTopicIds="32755205"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.environments.problemusingcustomdockerimagesordockerfile"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem using custom Docker images or Dockerfile

## **Recommended Steps**
### Docker image build failure
For the majority of the image build failures the root cause can be found in the image build log. You can find the image build log from the portal (20_image_build_log.txt) or from your ACR tasks runs logs.

In most cases, it is easy to reproduce the error locally. Please check try one of the following setuptools:

* install conda dependency locally `conda install suspicious-dependency==X.Y.Z`
* install pip dependency locally `pip install suspicious-dependency==X.Y.Z`
* try to materialize the entire environment `conda create -f conda-specification.yml`

Base image updates can result cache invalidation if the referenced tag was updated. If that behavior is not desired, please reference the base image including the digest, i.e. `my/repository:mytag@sha256:digest`

## **Recommended Documents**
If you are experiencing any problem using custom Docker images or Dockerfile, here is a list of additional resources which may be helpful:
* [Train a model with a custom Docker image](https://docs.microsoft.com/azure/machine-learning/how-to-train-with-custom-image)
* [Deploy a model using a custom Docker image](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-custom-docker-image#use-a-custom-base-image)
* [How to use environments](https://docs.microsoft.com/azure/machine-learning/how-to-use-environments#create-an-environment)
* [Concept overview](https://docs.microsoft.com/azure/machine-learning/concept-environments)
* [SDK documentation](https://docs.microsoft.com/python/api/azureml-core/azureml.core.environment)
