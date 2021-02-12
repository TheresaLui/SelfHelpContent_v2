<properties
	pageTitle="Azure-SSIS IR Customized Setup Issues"
	description="Troubleshooting Azure-SSIS IR Management - Customized Setup Issues"
	service="microsoft.datafactory"
	resource="factories"
	authors="chinadragon0515"
	ms.author="dashe"
	articleId="datafactory-newtree-ssis-ir-management-customized-setup.md"
	displayOrder="10"
	selfHelpType="generic"
	supportTopicIds="32680894"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Azure-SSIS IR Customized Setup Issues

The ADF Portal can be used to check the result of Azure SSIS IR start and there is detail error message shows on the ADF portal. The start result can also be retrieved via Azure powershell command.

## **Recommended Steps**

* Get the error code in the error message and then search the [troubleshoot document](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-management-troubleshoot) of the error code and find the detail cause and solution
* Custom setup provides an interface to add your own setup steps during the provisioning or reconfiguration of your SSIS IR. For more information, see [Customize setup for the Azure-SSIS Integration Runtime](https://docs.microsoft.com/azure/data-factory/how-to-configure-azure-ssis-ir-custom-setup).
* Make sure your container contains only the necessary custom setup files; all the files in the container will be downloaded onto the SSIS IR worker node. We recommend that you test the custom setup script on a local machine to fix any script execution issues before you run the script in SSIS IR.
* The custom setup script container will be checked while IR is running, because SSIS IR is regularly updated. This updating requires access to the container to download the custom setup script and install it again. The process also checks whether the container is accessible and whether the main.cmd file exists.
* For any error that involves custom setup, you'll see a CustomSetupScriptFailure error code with sub code like CustomSetupScriptBlobContainerInaccessible or CustomSetupScriptNotFound

### CustomSetupScriptBlobContainerInaccessible

This error means that SSIS IR can't access your Azure blob container for custom setup. Make sure the SAS URI of the container is reachable and has not expired.

Stop the IR if it's running, reconfigure the IR with new custom setup container SAS URI, and then restart the IR.

### CustomSetupScriptNotFound

This error means that SSIS IR can't find a custom setup script (main.cmd) in your blob container. Make sure that main.cmd exists in the container, which is the entry point for custom setup installation.

### CustomSetupScriptExecutionFailure

This error means the execution of custom setup script (main.cmd) failed. Try the script on your local machine first, or check the custom setup execution logs on your blob container.

### CustomSetupScriptTimeout

This error indicates an execute custom setup script timeout. Make sure that your script can be executed silently, and no interactive input needed, and make sure your blob container contains only the necessary custom setup files. It is recommended to test the script on local machine first. You should also check the custom setup execution logs in your blob container. The maximum period for custom setup is 45 minutes before it times out, and the maximum period includes the time to download all files from your container and install them on SSIS IR. If you need a longer period, raise a support ticket.

### CustomSetupScriptLogUploadFailure

This error means that the attempt to upload custom setup execution logs to your blob container failed. This problem occurs either because SSIS IR doesn't have write permissions to your blob container or because of storage or network issues. If custom setup is successful, this error won't affect any SSIS function, but the logs will be missing. If custom setup fails with another error, and the log isn't uploaded, we will report this error first so that the log can be uploaded for analysis. Also, after this issue is resolved, we will report any more specific issues. If this issue is not resolved after a retry, contact the Azure Data Factory support team.

## **Recommended Documents**

* [Customize setup for the Azure-SSIS integration runtime](https://docs.microsoft.com/azure/data-factory/how-to-configure-azure-ssis-ir-custom-setup)
* [Install paid or licensed custom components for the Azure-SSIS integration runtime](https://docs.microsoft.com/azure/data-factory/how-to-develop-azure-ssis-ir-licensed-components)
