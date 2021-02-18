<properties
	pageTitle="Service Connections"
	description="Issues with running tests in your pipeline using any of the testing frameworks, analyzing coverage using any of the code coverage frameworks, or publishing reports thereof."
	infoBubbleText="Azure Pipelines issues related to testing tasks, results, reports and code coverage"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AZDevOpsTestingCodeCoverage"
	supportTopicIds="32742330"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues with testing tasks, results, reports and code coverage

## **Recommended Steps**

Resolve many common issues with these steps.

* **I want to configure Azure pipeline to run Web UI test**

    [Refer to this document](https://docs.microsoft.com/azure/devops/pipelines/test/continuous-test-selenium?view=azure-devops).

* **My test results are published however, no code coverage data available even though the code coverage file is being created after the build.**

    This happens when mixed versions of Visual Studio are used to build and run tests. Ensure that the platform and configurations used for running the build and tests are the same version in the pipeline. 

* **I would like to link the automation tests that are executed during the pipeline with that of my test plan for a NodeJS/Java application**

    Associating the test case is supported only for the MSTest framework for Node.js and Java-based applications. This is present in a test case under the **Associated Automation** option. We cannot link it with the test plan option in Azure DevOps Services. However, you can execute the tests by using a third-party tool, which makes use of the [traceability option](https://docs.microsoft.com/azure/devops/pipelines/test/requirements-traceability?view=azure-devops) available in Azure Pipelines to display the reports.

* **My gradle build step fails even after all the test cases passing**

    There is a possibility that a few tests are failing and passing on rerun. In such scenarios, you can ignore flaky tests in pass percentage calculation by enabling the [flaky tests](https://docs.microsoft.com/azure/devops/pipelines/test/flaky-test-management?view=azure-devops).

* **I'm unable to fetch the Unit Test task's result and coverage reports**

    Use the relevant options in [this task](https://docs.microsoft.com/azure/devops/pipelines/tasks/build/dotnet-core-cli?view=azure-devops) to perform the test and publish the results respectively.

* **I'm unable to publishing code coverage results on the Azure DevOps UI and there is no documentation regarding the same**

    The feature to have code coverage as part of DevOps UI by default is under development. If you are using .NET Core projects, kindly make use .NET Core task which would give you code coverage in the build logs, but not in the Azure DevOps UI. [Publish code coverage result task](https://docs.microsoft.com/azure/devops/pipelines/tasks/test/publish-code-coverage-results?view=azure-devops) supports coverage result formats such as Cobertura and JaCoCo. To use this task you would need to use a code coverage tool as part of your project solution. For .NET projects, you may add a Nuget package to get the tool added to generate code coverage file required by either Cobertura or JaCoCo. Cobertura or JaCoCo would then populate the data to the code coverage tab.

## **Recommended Documents**

* [Review code coverage results](https://docs.microsoft.com/azure/devops/pipelines/test/review-code-coverage-results?view=azure-devops)
* [UI test with Selenium](https://docs.microsoft.com/azure/devops/pipelines/test/continuous-test-selenium?view=azure-devops)
* [Associate automated tests with test cases](https://docs.microsoft.com/azure/devops/test/associate-automated-test-with-test-case?view=azure-devops)
* [Run automated tests from test plans](https://docs.microsoft.com/azure/devops/test/run-automated-tests-from-test-hub?view=azure-devops)
* [Visual Studio Test task](https://docs.microsoft.com/azure/devops/pipelines/tasks/test/vstest?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net)

