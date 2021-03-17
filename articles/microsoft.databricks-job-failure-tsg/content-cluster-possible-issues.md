<properties
	pageTitle="Cluster possible issues"
	description="Cluster possible issues"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="dda3e6a1-82e7-4b74-8e84-486056021695"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Cluster possible issues

If the job failed prematurely at cluster creation stage, please collect cluster details and check the following:

1. Are there any throttling or issues reported in ASC insights?
2. From ASC, go to the Resource under Resource Explorer -> Cluster Resources tab -> Specify issue time frame and run diagnostics. Find the cluster and check the provisioning status and errors.
3. Check cluster event logs in customer workspace

There is more than one possible root cause. Please proceed according to user-facing errors below.

**Azure Network**

1. NRP throttling 

    ```
    Subscription XXX was used to perform too many calls within last 5 minutes. The number of calls exceeds Microsoft. Network throttling limit. or Encountered Azure Resource provider throttling. Please try again later.
    ```

2. Sporadic VM network issues/partitions 

    ```
    Cluster terminated. Reason: Metastore Component Unhealthy
    ```

**Azure Compute**

3. Slow/unreliable VM launch 

    ```
    Cluster is running but X nodes could not be acquired.
    ```

**Azure Storage**

4. Storage throttling 

    ```
    Files and folders are being created at too high a rate.
    ```

**Databricks Launch Failures**

5. Cluster timeout

    ```
    The Spark driver failed to start within 300 seconds.
    ```

6. Cluster timeout due to Init

    ```
    The cluster could not be started in 50 minutes. Cause: Timed out with exception after <xx> attempts.
    ```

7. Cloud provider launch failure 

    ```
    The client 'xxx' with object id 'xxx' does not have authorization to perform action 'Microsoft.Network/publicIPAddresses/write' over scope '/subscriptions/xxx...')
    ```

**Azure Subscription Limit**

8. Quota limit reached (cores, public IPs,...)

    ```
    Cloud Provider Launch Failure: A cloud provider error was encountered while setting up the cluster. See the Databricks guide for more information.
    Azure error code: OperationNotAllowed
    Azure error message: Operation results in exceeding quota limits of Core. Maximum allowed: xx, Current in use: xx, Additional requested: x.
    ```

