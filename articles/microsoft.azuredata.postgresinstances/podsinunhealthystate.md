<properties
  pagetitle="Pods are in an Unhealthy State"
  service="microsoft.azuredata"
  resource="postgresinstances"
  ms.author="pookam"
  selfhelptype="Generic"
  supporttopicids="32747915"
  productpesids="17124"
  cloudEnvironments="public, fairfax, usnat, ussec"
  articleid="8b1ae136-b9b6-409d-82f9-34d2913c7ed6"
  ownershipid="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale" />
# Pods are in an Unhealthy State

Check if any events are reported for the pods that your server group is running in by using the below steps.

## **Recommended Steps**

* Get the list of pods: `Kubectl get pods`
* **Describe** each of the pods of your server group. The name of the pods follow the pattern server group name - x where x is a number starting at 0: 

    * 0 is the **coordinator **node
    * X are the **worker **nodes        
    
- For each of the pods run: `kubectl describe pod <server group name> -x`
- Look at the section **Events** at the bottom of the output and see if any problem is indicated. Troubleshoot this problem.
- Alternatively run `kubectl get events` and see if any problem is indicated
- If the problem appears after you changed the configuration of the server group (scale up/down, or server parameters):

  * Revert the change 
  * If this solves the problem, review the configuration change you desired and adjust it to what your Kubernetes cluster can deliver
  * If this does not solve the problem, reach out to your Kubernetes team and then to the Microsoft support services if the issue persists

 ## **Recommended Documents**

- [Read about troubleshooting pods](https://kubernetes.io/docs/tasks/debug-application-cluster/debug-pod-replication-controller/)
- [Debug Running Pods](https://kubernetes.io/docs/tasks/debug-application-cluster/debug-running-pod/)
