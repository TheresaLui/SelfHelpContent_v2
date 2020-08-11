<properties
	pageTitle="Using scripts in Azure Pipelines"
	description="Azure Pipelines issues related to command line scripts"
	infoBubbleText="Azure Pipelines issues related to command line scripts"
	service="microsoft.visualstudio"
	resource="account"
	authors="vtbassmatt"
	ms.author="macoope"
	articleId="AZDevOpsPipelinesCmdLine"
	supportTopicIds="32742326"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipelines issues related to command line scripts

3 out of every 5 problems related to triggers were solved using the solutions below.

## **Recommended Steps**

You may be having trouble running command-line tools or scripts in Azure Pipelines.

Follow through all the steps before you create a support ticket. If you do need to create a ticket after completing the diagnostic steps, provide information about the path you took and results of the steps you ran in your ticket to expedite the resolution of your problem.

* I set environment variables, source Bash scripts, or install PowerShell modules in a step, and they aren't available in subsequent steps.

	- Azure Pipelines starts each step in a fresh, new process. Changes made to the environment are not persisted between steps.
  - Move your environmental changes and use of those changes into the same step.
  - Read more about [how pipeline runs, specifically steps, are executed](https://docs.microsoft.com/azure/devops/pipelines/process/runs#run-each-step).
	
* I am using a preinstalled tool, but certain options aren't working.

  - The preinstalled tool might be a different version from the one that's installed on your local machine. If it's older, it may have fewer options. If it's newer, the options could have been renamed.
	- Check the version number of the installed tool. Often this is done by passing `-V`, `-v`, or `--version` to the tool.
  - Consult the documentation for the precise installed version of the tool to see what options are available.

* I am attempting to connect to or copy files to a remote machine, and it's not working.

	- Check that you can connect or copy files from the host machine to the remote machine outside of a pipeline. Often, the problem isn't with Azure Pipelines, it's with configuration on the host or the network.
  - Run agent diagnostics to confirm the agent's access to the network. `./run.sh --diagnostics` on Linux and macOS; `./run.cmd --diagnostics` on Windows.
  - Make sure you have appropriate permissions on the remote machine. On Linux, you may need to be in the appropriate group to allow SSH connections, or may need to be listed in `sudoers`.
  - Make sure the remote machine's firewall settings allow the connection, and that the remote network allows inbound connections.
  - Make sure that, if you require a proxy on the host machine, that it's configured properly. Also make sure the [agent is configured with the proxy details](https://docs.microsoft.com/azure/devops/pipelines/agents/proxy).
  - If you're using  WinRM, make sure the WinRM service is [installed and running on the remote machine](https://docs.microsoft.com/windows/win32/winrm/installation-and-configuration-for-windows-remote-management).

* A script or tool I'm running works locally but complains about missing files when run in a pipeline.

	- The layout of files may be different on a pipelines agent than on your local machine.
  - You can try [searching for the missing files](https://docs.microsoft.com/azure/devops/pipelines/troubleshooting/troubleshooting#my-pipeline-is-failing-on-a-command-line-step-such-as-msbuild).

## **Recommended Documents**

* [Troubleshoot pipeline runs](https://docs.microsoft.com/azure/devops/pipelines/troubleshooting/troubleshooting)
* [Linux agent diagnostics](https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/v2-linux#diagnostics)
* [macOS agent diagnostics](https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/v2-osx#diagnostics)
* [Windows agent diagnostics](https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/v2-windows#diagnostics)
* [Azure DevOps Services Status](https://status.dev.azure.com)
