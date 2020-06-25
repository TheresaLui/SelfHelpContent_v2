<properties 
    pageTitle="How do I automatically track dependencies?"
    description="Quick how-to guide for dependency tracking"
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights_trackdependencies"
    displayOrder="140"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32632981,32729605"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# How do I automatically track dependencies

For all SDKs there is a minimal level of dependency tracking that will cover the most common types of dependencies. For example, .NET will collect SQL and HTTP dependencies--including services built on HTTP such as Storage--without much configuration. For Java you would need to install the Java agent. The steps below will cover the most common monitoring scenarios. Node.JS and JavaScript natively support these without additional configuration.

## **Recommended Steps**

**App Service**<br>

1. Review the setup [guide](https://docs.microsoft.com/azure/azure-monitor/app/azure-web-apps#enable-application-insights) for common problems and solutions
2. Navigate to your App Service
3. Click the Application Insights item on the menu to the left
4. If not enabled, click Enable and create or link a resource 
5. Select the Recommended configuration
6. Optionally, enable SQL Commands to see the SQL being executed

**On-premises .NET applications**<br>

1. Review the installation [guide](https://docs.microsoft.com/azure/azure-monitor/app/monitor-performance-live-website-now)
2. On your IIS web server, sign in with administrator credentials.
3. If Application Insights Status Monitor is not already installed, [download and run the installer](https://docs.microsoft.com/azure/azure-monitor/app/monitor-performance-live-website-now#download)
4. In Status Monitor, select the installed web application or website that you want to monitor. Sign in with your Azure credentials.
5. Restart IIS.

**On-premises Java applications**<br>

1. Review the agent installation [guide](https://docs.microsoft.com/azure/azure-monitor/app/java-agent)
2. On the machine running your Java server, [download the agent](https://github.com/Microsoft/ApplicationInsights-Java/releases/latest). Please ensure to download the same version of Java Agent as Application Insights Java SDK core and web packages.
3. Edit the application server startup script, and add the following JVM: `-javaagent:PATHTOAGENTJAR`
4. Restart JVM

**Node.js**<br>

1. Add `.setAutoDependencyCorrelation(true)` to your initialization

**JavaScript**<br>
AJAX dependencies are automatically captured

**Known Issues**<br>

1. For .NET if there is a version mismatch some dependencies may not be captured or correlated correctly. Ensure all versions of the agent and SDK are the same.
2. For Java the agent requires the XML file to load, please [check the documentation](https://docs.microsoft.com/azure/azure-monitor/app/java-agent) for examples
3. For Java, not all database and HTTP clients are implemented [check the documentation](https://docs.microsoft.com/azure/azure-monitor/app/java-agent) for details
4. For JavaScript we hook on to the XMLHttpRequest object, other libraries that do this can cause conflicts.

## **Recommended Documents**
* [Setup App Service](https://docs.microsoft.com/azure/azure-monitor/app/azure-web-apps#enable-application-insights)<br>
* [Status Monitor](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-performance-live-website-now)<br>
* [Java Agent](https://docs.microsoft.com/azure/azure-monitor/app/java-agent)<br>
* [Node.js](https://docs.microsoft.com/azure/azure-monitor/app/nodejs)
* [Application Insights Troubleshooting](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net-troubleshoot-no-data)<br>
