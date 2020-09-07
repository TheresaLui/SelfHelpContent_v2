<properties
	pageTitle="worker role (paas)/Deployment/Deployment taking longer"
	description="worker role (paas)/Deployment/Deployment taking longer"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="ChiragPavecha"
	ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32565476"
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="78d8ddfd-f265-4a78-ae69-7514b854ee36"
	ownershipId="Compute_CloudServices_Content"
/>

# worker role (paas)/Deployment/Deployment taking longer

**Awareness**

>We are currently experiencing high demand for specific regions. For further information, please review our [commitment to customers and Microsoft Cloud Services continuity](https://azure.microsoft.com/blog/update-2-on-microsoft-cloud-services-continuity/).<br>

## **Recommended Steps**

For general troubleshooting, please follow these guides:<br>

1. Understand the common scenarios of Allocation Failures for Cloud Services ([Allocation Failure](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures#common-issues))<br>
2. If it’s a new deployment try to deploy in another region or use another size in the given region. Check available ([sizes](https://docs.microsoft.com/azure/cloud-services/cloud-services-sizes-specs)) and ([regions](https://azure.microsoft.com/global-infrastructure/services/?products=cloud-services)) for Cloud Services role.<br>
3. If it’s an upgrade or scaling of an existing deployment, try one of these ([solutions](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures#solutions))<br>

## **Recommended Documents**

* [Understand what happen when you deploy on Windows Azure](http://stackoverflow.com/questions/30270136/why-azure-deployment-from-visual-studio-takes-so-long) <br>
* [Frequently Asked Questions on Cloud Services Deployment](https://docs.microsoft.com/azure/cloud-services/cloud-services-deployment-faq)<br>
* [Possible Solutions for Cloud Services Allocation Failures](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures#solutions)<br>
* [Available sizes and options for Cloud Service role instances (web and worker roles)](https://docs.microsoft.com/azure/cloud-services/cloud-services-sizes-specs)<br>
* [General REST and retry guidelines](https://docs.microsoft.com/azure/architecture/best-practices/retry-service-specific#general-rest-and-retry-guidelines)<br>
* [Allocation Failure Remediations](https://azure.microsoft.com/blog/allocation-failure-and-remediation/)
