<properties
	pageTitle="Machine Learning Services for SQL Managed Instance (Preview)/Other issue or 'How To' questions"
	description="Machine Learning Services for SQL Managed Instance (Preview)/Other issue or 'How To' questions"
	infoBubbleText="Machine Learning Services for SQL Managed Instance (Preview)/Other issue or 'How To' questions"
	service="microsoft.sql"
	resource="servers"
	authors="vitomaz-msft"
	ms.author="vitomaz"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32742351"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmi-machinelearning-other"
	ownershipId="AzureData_AzureSQLMI"
/>

**How do I sign up for the Preview?**
In your request, state that you would like to be enrolled into limited public preview of Machine Learning for SQL Managed Instance with these details: logical server name, region, and subscription ID.
Once you're enrolled in the program, Microsoft will onboard you to the public preview and enable Machine Learning Services for your existing or new database.
Machine Learning Services in SQL Managed Instance is not recommended for production workloads during the public preview.

**How long will it take for me to get onboarded for the Preview once I submit a request?**
The enrollment is subject to verification, availability of seats and internal approval. The preview will be available for enrollment for the specific regions on the below dates. This process might take up to 5 business days from the time the requested region is open for enrollment.  
The onboarding dates for each region are:
- 6/3/2020 for West Europe
- 6/13/2020 for Australia Central, Australia East, Canada Central, China North 1, China North 2, East Asia, East US, East US2, France South, Germany North, Germany North East, India Central, India West, Japan East, Korea south, NorthCentralUS, Norway East, SouthAfrica  North, Switzerland North, UAE Central, UK South, West US2
- 6/30/2020 for Australia Central 2, Australia southeast, Canada East, Central US, China East, China East 2, France Central, Germany Central, Germany West Central, India South, Japan West, Korea Central, North Europe, Norway West, SouthAfrica West, SouthCentralUS, SouthEast Asia, Switzerland West, UAE North, UK West, West US
 
**Is the Preview Available for Azure SQL Database as well?**
No. This preview is available only for Azure SQL Managed Instance.
As of 30 June 2020, support will be discontinued for Azure SQL Database , Machine Learning Services with R (preview) - and the preview will not be released for general availability. R scripts in use after 30 June 2020 will not work. To continue working with machine learning in Azure SQL, sign up for Machine Learning Services in Azure SQL Managed Instance (preview).
[Discontinued Preview](https://docs.microsoft.com/azure/azure-sql/database/machine-learning-services-overview)
 
**Preview Limitations**
Machine Learning Services is a feature of Azure SQL Managed Instance that's currently in public preview. This preview functionality is initially available in a limited number of regions in the US, Asia Europe, and Australia with additional regions being added later.
This preview version is provided without a service level agreement, and it's NOT recommended for production workloads. Certain features might not be supported or might have constrained capabilities.

During the preview, the service has the following limitations:
- Loopback connections do not work (see Loopback connection to SQL Server from a Python or R script).
- External Resource pools are not supported.
- Only Python and R are supported. External languages such as Java cannot be added.
- Scenarios using the Message Passing Interface (MPI) are not supported.
- In case of a Service Level Objective (SLO) update, please update the SLO and raise a support ticket to re-enable the dedicated resource limits for R/Python.
 
For more details check: [Preview Limitations](https://docs.microsoft.com/azure/azure-sql/managed-instance/machine-learning-services-differences#preview-limitations)
 
**How is Resource Governance Managed when we enable Machine Learning Services for Azure SQL Managed Instance**
It is not possible to limit R resources through Resource Governor and external resource pools.
During the public preview, R resources are set to a maximum of 20% of the SQL Managed Instance resources, and depend on which service tier you choose. For more information, see Azure SQL Database purchasing models
[Resource Governance](https://docs.microsoft.com/azure/azure-sql/managed-instance/machine-learning-services-differences#resource-governance)
 
**What additional steps do I have to perform to use Machine Learning Services on Azure SQL Managed Instance**
There is no need to configure external scripts enabled via sp_configure. Once you are signed up for the preview, machine learning is enabled for your SQL database.
In case of a Service Level Objective (SLO) update, please update the SLO and raise a support ticket to re-enable the dedicated resource limits for R/Python.
 
**What if I get message "External script execution for 'R' script ran out of resources" or "A R' script error occurred during execution of 'sp_execute_external_script" ?**
  
If there is insufficient memory available for R, you will get an error message. Common error messages are:
Unable to communicate with the runtime for 'R' script for request id: *******. Please check the requirements of 'R' runtime
 
'R' script error occurred during execution of 'sp_execute_external_script' with HRESULT 0x80004004. ...an external script error occurred: "..could not allocate memory (0 Mb) in C function 'R_AllocStringBuffer'"
 
An external script error occurred: Error: cannot allocate vector of size.> 
 
Memory usage depends on how much is used in your R scripts and the number of parallel queries being executed. If you receive the errors above, you can scale your database to a higher service tier to resolve this. 
In case of a Service Level Objective (SLO) update, please update the SLO and raise a support ticket to re-enable the dedicated resource limits for R/Python.
[Script Errors due to insufficient Memory](https://docs.microsoft.com/azure/azure-sql/managed-instance/machine-learning-services-differences#insufficient-memory-error). 
 
 
**Key differences between Machine Learning Services in Azure SQL Managed Instance and SQL Server**
The functionality of Machine Learning Services in Azure SQL Managed Instance (preview) is nearly identical to SQL Server Machine Learning Services , however the key differences are listed below
[Key Differences](https://docs.microsoft.com/azure/azure-sql/managed-instance/machine-learning-services-differences#packages)


## **Recommended Documents**
 
   - Using sp_execute_external_script stored procedure
   sp_execute_external_script stored procedure executes a script provided as an input argument to the procedure, and is used with Machine Learning Services and Language Extensions. For Azure SQL Managed Instance, only Python and R are supported. External languages such as Java cannot be added. For more info on usage see [sp_execute_external_script](https://docs.microsoft.com/sql/relational-databases/system-stored-procedures/sp-execute-external-script-transact-sql?view=sql-server-ver15)

   - How do I install a new Package
   Most common open-source R packages are pre-installed in Machine Learning Services. In addition to the pre-installed packages, you can also install additional packages.
      - [Install new R packages with sqlmlutils](https://docs.microsoft.com/sql/machine-learning/package-management/install-additional-r-packages-on-sql-server?view=sql-server-ver15)
      - [Install Python packages with sqlmlutils](https://docs.microsoft.com/sql/machine-learning/package-management/install-additional-python-packages-on-sql-server?view=sql-server-ver15) 
 
    
   - Quickstarts & Tutorials
      - [Quickstart: Run simple R scripts with SQL machine learning](https://docs.microsoft.com/sql/machine-learning/tutorials/quickstart-r-create-script?context=/azure/azure-sql/managed-instance/context/ml-context&view=sql-server-ver15)
      - [Quickstart: Run simple Python scripts with SQL machine learning](https://docs.microsoft.com/sql/machine-learning/tutorials/quickstart-python-create-script?context=/azure/azure-sql/managed-instance/context/ml-context&view=sql-server-ver15)
      - [R tutorials for SQL machine learning](https://docs.microsoft.com/sql/machine-learning/tutorials/r-tutorials?view=sql-server-ver15)
      - [Python tutorials for SQL machine learning](https://docs.microsoft.com/sql/machine-learning/tutorials/python-tutorials?view=sql-server-ver15)
