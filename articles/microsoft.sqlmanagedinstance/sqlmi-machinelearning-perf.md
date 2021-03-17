<properties
	pageTitle="Machine Learning Services for SQL Managed Instance (Preview)/Performance issues and timeouts"
	description="Machine Learning Services for SQL Managed Instance (Preview)/Performance issues and timeouts"
	infoBubbleText="Machine Learning Services for SQL Managed Instance (Preview)/Performance issues and timeouts"
	service="microsoft.sql"
	resource="servers"
	authors="vitomaz-msft"
	ms.author="vitomaz"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32742352"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmi-machinelearning-perf"
	ownershipId="AzureData_AzureSQLMI"
/>

# Performance issues and timeouts

### **Preview Limitations**
Machine Learning Services is a feature of Azure SQL Managed Instance that's currently in public preview. This preview functionality is initially available in a limited number of regions in the US, Asia, Europe, and Australia with additional regions being added later.
This preview version is provided without a service level agreement, and it's NOT recommended for production workloads. Certain features might not be supported or might have constrained capabilities.

During the preview, the service has the following limitations:
- Loopback connections do not work (see Loopback connection to SQL Server from a Python or R script).
- External Resource pools are not supported.
- Only Python and R are supported. External languages such as Java cannot be added.
- Scenarios using the Message Passing Interface (MPI) are not supported.
- In case of a Service Level Objective (SLO) update, please update the SLO and raise a support ticket to re-enable the dedicated resource limits for R/Python.
 
For more details check: [Preview Limitations](https://docs.microsoft.com/azure/azure-sql/managed-instance/machine-learning-services-differences#preview-limitations)
 
### **How is Resource Governance Managed when we enable Machine Learning Services for Azure SQL Managed Instance**
It is not possible to limit R resources through Resource Governor and external resource pools.
During the public preview, R resources are set to a maximum of 20% of the SQL Managed Instance resources, and depend on which service tier you choose. For more information, see Azure SQL Database purchasing models
[Resource Governance](https://docs.microsoft.com/azure/azure-sql/managed-instance/machine-learning-services-differences#resource-governance)
 
### **What additional steps do I have to perform to use Machine Learning Services on Azure SQL Managed Instance**
There is no need to configure external scripts enabled via sp_configure. Once you are signed up for the preview, machine learning is enabled for your SQL database.
In case of a Service Level Objective (SLO) update, please update the SLO and raise a support ticket to re-enable the dedicated resource limits for R/Python.
 
### **What if I get message "External script execution for 'R' script ran out of resources" or "A R' script error occurred during execution of 'sp_execute_external_script" ?**
  
If there is insufficient memory available for R, you will get an error message. Common error messages are:
Unable to communicate with the runtime for 'R' script for request id: *******. Please check the requirements of 'R' runtime
 
'R' script error occurred during execution of 'sp_execute_external_script' with HRESULT 0x80004004. ...an external script error occurred: "..could not allocate memory (0 Mb) in C function 'R_AllocStringBuffer'"
 
An external script error occurred: Error: cannot allocate vector of size.> 
 
Memory usage depends on how much is used in your R scripts and the number of parallel queries being executed. If you receive the errors above, you can scale your database to a higher service tier to resolve this. 
In case of a Service Level Objective (SLO) update, please update the SLO and raise a support ticket to re-enable the dedicated resource limits for R/Python.
[Script errors due to insufficient memory](https://docs.microsoft.com/azure/azure-sql/managed-instance/machine-learning-services-differences#insufficient-memory-error). 
 
 
### **Key differences between Machine Learning Services in Azure SQL Managed Instance and SQL Server**
The functionality of Machine Learning Services in Azure SQL Managed Instance (preview) is nearly identical to SQL Server Machine Learning Services, however the key differences are listed below
[Key differences](https://docs.microsoft.com/azure/azure-sql/managed-instance/machine-learning-services-differences#packages)


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
