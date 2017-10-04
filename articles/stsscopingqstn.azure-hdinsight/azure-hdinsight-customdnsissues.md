<properties
   pageTitle="Scoping questions for HDInsight Custom DNS Issues"
   description="Scoping questions for HDInsight Custom DNS Issues"
   authors="ansiva"
   selfHelpType="supportTopicBasedScopingQuestions"
   supportTopicIds="32588502"
  productPesIds="15078"
  cloudEnvironments="public"
/>
# HDInsight Spark Issues
* Did you follow the troubleshooting steps at ---?
* What is the output for the following commands? (ssh into the cluster head node to run these):
** `Hostname -f`
** `nslookup <headnode_fqdn>` (e.g.nslookup hn1-hditest.5h6lujo4xvoe1kprq3azvzmwsd.hx.internal.cloudapp.net)
** `dig @168.63.129.16 <headnode_fqdn>` (e.g.dig @168.63.129.16 hn1-hditest.5h6lujo4xvoe1kprq3azvzmwsd.hx.internal.cloudapp.net)