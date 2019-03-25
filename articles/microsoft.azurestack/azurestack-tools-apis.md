<properties
    pageTitle="Azure Stack vm-windows.md"
    description=""
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629184,32629200"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-tools-apis"
/>

# Azure Stack CLI

The Azure CLI is a command-line tool providing a great experience for managing Azure Stack resources. The CLI is designed to make scripting easy, query data, support long-running operations, and more.<br>

You will need to install the Azure CLI, Python, add trust the Azure Stack CA root certificate, and use the appropriate API Profile.<br>

## **Recommended steps**

1. Get the Azure Stack CA root certificate from the Azure Stack operator. If you are the operator, you can find the instructions in the following article [Enable Azure CLI for Azure Stack users](https://docs.microsoft.com/azure/azure-stack/azure-stack-cli-admin).<br>
2. Install Azure CLI on your development workstation. Use the steps described in the [Install CLI](https://docs.microsoft.com/cli/azure/install-azure-cli) article.<br>
3. Install Python 3.6 or later on your development workstation. You can find the instructions and the installation file at [Python.org](https://www.python.org/downloads).<br>
4. Follow the instruction in [Use API version profiles with Azure CLI in Azure Stack](https://docs.microsoft.<br>com/azure/azure-stack/user/azure-stack-version-profiles-azurecli2) to trust your certificate, append it to your existing Python certificate, get the VM alias endpoint, and connect to Azure Stack.<br>

## **Recommended documents**

[Enable Azure CLI for Azure Stack users](https://docs.microsoft.com/azure/azure-stack/azure-stack-cli-admin)<br>
[Install the Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli)<br>
[Use API version profiles with Azure CLI in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-azurecli2)<br>
[Manage API version profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles)

# Azure Stack JSON

JSON (JavaScript Object Notation) data is represented as key-value pairs in a semi-structured format. JSON is often compared to XML, as both are capable of storing data in hierarchical format, with child data represented inline with its parent. Both are self-describing and human readable, but JSON documents tend to be much smaller, leading to their popular use in online data exchange, especially with the advent of REST-based web services.<br>

Azure and Azure Stack provide several solutions for working with JSON files, depending on your needs. The primary landing place for these files is either Azure Storage or Azure Data Lake Store. Most Azure services that work with these and other text-based files integrate with either object storage service. In some situations, however, you may opt to directly import the data into Azure SQL or some other data store. SQL Server has native support for storing and working with JSON documents.<br>

## **Recommended steps**

1. You can review specific storage options for Azure Stack. For information see [Azure Stack storage: Differences and considerations](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-acs-differences).<br>
2. You can find tips for working with Azure, Azure Stack, and JSON and CSV in the article [Working with CSV and JSON files for data solutions](https://docs.microsoft.com/azure/architecture/data-guide/scenarios/csv-and-json).<br>
3. You may want to review the steps to [Import JSON documents into SQL Server](https://docs.microsoft.com/sql/relational-databases/json/import-json-documents-into-sql-server?view=sql-server-2017).<br>
4. You can use SQL Server to transform JSON data. For more information see [Parse and Transform JSON Data with OPENJSON (SQL Server)](https://docs.microsoft.com/sql/relational-databases/json/convert-json-data-to-rows-and-columns-with-openjson-sql-server?view=sql-server-2017).<br>

## **Recommended documents**

[Introducing JSON](https://json.org/)<br>
[ECMA-404 The JSON Data Interchange Standard.](http://www.ecma-international.org/publications/files/ECMA-ST/ECMA-404.pdf)<br>
[JSONLint](https://jsonlint.com/?json=)

# Azure Stack REST API

The Azure Stack Admin REST API requires your client to authenticate to the Microsoft Azure sign-in endpoint. The endpoint returns a token to use in the header of every request sent to the Azure Stack API. Microsoft Azure uses Oauth 2.0.<br>

There are a two main ways that you may need to interact with the API.<br>

1.  **Azure Stack Admin API**<br>

	Azure Stack Admin APIs provide REST API interfaces for each Resource Provider that ships with Azure Stack inbox, for performing operations on selected entities, such as Scale Unit Nodes, Alerts, Updates, Backup, Marketplace, Subscriptions, Offers, and much more.<br>

2.  **Azure resource providers (RP)s with API profiles for Azure Stack**<br>

    API profiles specify the Azure resource provider and the API version for Azure REST endpoints. You can create custom clients in different languages using API profiles. Each client uses an API profile to contact the correct resource provider and API version for Azure Stack.<br>

## **Recommended steps**

If you are having issues with the API, make sure that you have the following elements in place for either the Admin or Azure Stack Resource Manger APIs.<br>

###  **Azure resource providers (RP)s with API profiles for Azure Stack**

1. [Get a token from Azure](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-rest-api-use#get-a-token-from-azure).<br>
2. Create an API request. For information, see [API queries](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-rest-api-use#api-queries).<br>
3. Find the specific call you would like to me by consulting the [Azure Stack Rest API Reference](https://docs.microsoft.com/rest/api/azure-stack).<br>

### **Azure Stack Admin API**

1. Review [How to call Azure REST APIs with Postman](https://docs.microsoft.com/rest/api/azure/) for steps on setting up authorization, your client, and the flow for sending a reqeust and receiving a return payload.<br>
2. Identify the current API profile for Azure Stack. You can review API profiles at [Resource provider API versions supported by profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-profiles-azure-resource-manager-versions).<br>
3. Construct your request with the API Profile.<br>

    For example, you might send an HTTPS GET request method for to an integrated system Azure Resource Manager provider by using request header fields that are similar to the following (note that the request body is empty):<br>
<br>
    ```REST  
    GET /subscriptions?api-version=2018–03-01-hybrid HTTP/1.1
    Authorization: Bearer <bearer-token>
    Host: https://management.<location>.ext-<machine-name>.masd.stbtest.microsoft.com
    ```
<br>

## **Recommended documents**

[Use the Azure Stack API](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-rest-api-use)<br>
[Azure Stack Admin API reference](https://docs.microsoft.com/rest/api/azure-stack/)<br>
[Manage API version profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles)<br>
[Resource provider API versions supported by profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-profiles-azure-resource-manager-versions)<br>
[Azure REST API Reference](https://docs.microsoft.com/rest/api/azure/)


# Azure Stack PowerShell

To work with Azure Stack, you must install Azure Stack compatible PowerShell modules. Compatibility is enabled through a feature called API profiles. However, Azure Stack  uses PowerShell in four different contexts. Successfully working with PowerShell requires managing these different contexts.<br>

## Azure Stack PowerShell contexts

**Azure PowerShell**<br>
Azure PowerShell provides a set of cmdlets that use the Azure Resource Manager model for managing your Azure resources. You can use it on your local machine and use it in any PowerShell session. For more information, [Overview of Azure PowerShell](https://docs.microsoft.com/powershell/azure/overview).<br>

**Azure Stack Powershell**<br>
Azure Stack PowerShell provides a set of cmdlets that use the Azure Resource Manager model for managing your Azure Stack resources. These resources require specific resources and version numbers and are different than the Azure PowerShell resources. You can use Azure Stack PowerShell on your local machine and use it in any PowerShell session. For more information, [Install PowerShell for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install).<br>

The Azure Stack Powershell uses API profiles to make sure that you are using the right resource provider and version when using cmdlets. API profiles provide a way to manage version differences between Azure and Azure Stack. An API version profile is a set of Azure Resource Manager PowerShell modules with specific API versions. Each cloud platform has a set of supported API version profiles. For example, Azure Stack supports a specific dated profile version such as 2018-03-01-hybrid, and Azure supports the latest API version profile. When you install as profile, the Azure Resource Manager PowerShell modules that correspond to the specified profile are installed. For more information, [Manage API version profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles).<br>

**Priviledge End Point**<br>
The Azure Stack operator uses the administrator portal, PowerShell, or Azure Resource Manager APIs for most day-to-day management tasks. However, for some less common operations, the operator needs to use the privileged endpoint (PEP). The PEP is a pre-configured remote PowerShell console that provides you with just enough capabilities to help the operator perform required tasks. For more information [Using the privileged endpoint in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-privileged-endpoint).<br>

**Azure Stack Tools**<br>
AzureStack-Tools is a GitHub repository that hosts PowerShell modules for managing and deploying resources to Azure Stack. If you are planning to establish VPN connectivity, you can download these PowerShell modules to the Azure Stack Development Kit, or to a Windows-based external client. For more information [Download Azure Stack tools from GitHub](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-download).<br>

## **Recommended steps**

1. Are you using the PowerShell in the right context? Review [the context](#azure-stack-powershell-contexts).<br>
2. Are your PowerShell modules conflicting with similar modules? You may want to [uninstall existing versions of the Azure Stack PowerShell modules](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?toc=%2Fen-us%2Fazure%2Fazure-stack%2Fuser%2FTOC.json&bc=%2Fen-us%2Fazure%2Fbread%2Ftoc.json#3-uninstall-existing-versions-of-the-azure-stack-powershell-modules).<br>
3. Are you using the correct API Profile. [Check your installed profiles](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-powershell#get-the-installed-profiles).<br>

## **Recommended documents**

[Install PowerShell for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install)<br>
[Overview of Azure PowerShell](https://docs.microsoft.com/powershell/azure/overview?view=azurermps-6.12.0)<br>
[Using the privileged endpoint in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-privileged-endpoint)<br>
[Use API version profiles for PowerShell in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-powershell)