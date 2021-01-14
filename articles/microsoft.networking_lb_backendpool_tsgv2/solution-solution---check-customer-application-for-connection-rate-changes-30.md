<properties
	  pageTitle="Solution - Check customer application for connection rate changes"
	  description="Solution - Check customer application for connection rate changes"
    service="Microsoft.Network"
     resource="Microsoft.Network/loadBalancers"
	  authors="dgoddard"
	  ms.author="dgoddard"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="6e37fd32-6fe8-4df7-aa2d-074d0cdf08dc"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Solution - Check customer application for connection rate changes

<!--issueDescription-->

Dear <Customer>,

Thank you for contacting us about your load balancer backend pool connectivity issue. We have reviewed diagnostics and configuration available to us. We observed an increase in the rate of SYN/FIN packets observed on your backend VM instances. This typically indicates that something caused your clients to re-connect to the server. The next step is to look in your application logs and telemetry to determine if there is an indication of what may have happened.

If you need additional support on this matter, please let us know.  

Best regards,

<!--/issueDescription-->

