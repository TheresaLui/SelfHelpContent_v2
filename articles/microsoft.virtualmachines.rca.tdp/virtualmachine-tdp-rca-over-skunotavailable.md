<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-skunotavailable"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.authors="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-skunotavailable"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because of a restriction on the SKU that you are trying to deploy.

* There are currently not enough cores of the VM Size Family you requested in this region.

An SKU defines the image used to create a virtual machine and is composed of the following:

- The disk image (operating system and version).
- The image size.
- The region where the VM is deployed.<br>

An SKU is unavailable when a region cannot accommodate the demand for a particular SKU. You have two options:

- Find an alternate SKU.
- Submit a subscription management support request.<br>

Over the past several months, we have experienced unprecedented demand for Azure in several regions. In some regions, the demand for a specific SKU may outstrip capacity. This should be a temporary situation as we are actively working to build out additional capacity. Sometimes we have to make the difficult decision to restrict certain offer types in a few regions until the demand can be accommodated.<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>

Also, if you have more subscriptions to whitelist, please share the subscription details and planned SKU size and numbers of VM’s / cores to deploy in the requested region.<br>

## Sample SKU availability queries

The following PowerShell, Azure CLI, and REST examples show how to query for a list of SKUs that match a desired size, disk image, and region. For details see the solutions in [Resolve errors for SKU not available](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors).<br>
, 
### PowerShell

``` PowerShell
Get-AzComputeResourceSku | where {$_.Locations.Contains("centralus") -and $_.Name.Contains("Standard_DS14_v2") }
```


### Azure CLI


### REST


## Related articles

* [Resolve errors for SKU not available](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors)
* [Region or SKU unavailable](https://docs.microsoft.com/azure/azure-supportability/sku-series-unavailable)<br>

