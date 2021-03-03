<properties
	pageTitle="Environment build fails"
	description="Environment build fails"
	infoBubbleText="Environment build fails"
	service="microsoft.machinelearning"
	resource="Docker and Python Package Management (Environments)"
	authors="saachigopal"
	ms.author="sagopal"
	supportTopicIds="32755203"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.environments.environmentbuildfails"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Environment build fails

## **Recommended Steps**
### Misaligned dependencies
* For production scenarios, it is strongly recommended to pin python dependencies to eliminate the risk of a broken environment as a result of image rebuild. Environment build will result in the latest python dependencies that satisfy the requirements at the time when the build happened.
* Remember to enable `Environment.python.user_managed_dependencies = True` if you want to disable the default Conda environment

### Image rebuild
* Image build will happen automatically upon experiment submission if the corresponding image is not cached. To manually submit cloud image build for an Environment, you need to register it first and call build on returned instance of the Environment: `myenv.register(workspace=ws).build(workspace=ws)`
* Changing the order of dependencies or channels in environment will result a new environment and will require a new image build
* If using a Docker image, see the image build log from the portal (20_image_build_log.txt) or from your ACR tasks runs logs

## **Recommended Documents**
If you are experiencing any environment build failures, here is a list of additional resources which may be helpful:
* [How to use environments](https://docs.microsoft.com/azure/machine-learning/how-to-use-environments)
* [Concept overview](https://docs.microsoft.com/azure/machine-learning/concept-environments)
* [SDK documentation](https://docs.microsoft.com/python/api/azureml-core/azureml.core.environment)
