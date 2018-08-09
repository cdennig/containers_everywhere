# Use Open Service Broker for Azure to creating an Azure SQL DB

This sample assumes that you have installed OSBA successfully to your Kubernetes cluster

<http://osba.sh/>

To create a SQLDb instance in Azure, first apply *service-instance.yaml*, afterwards use *service-binding.yaml* to be able to use the SQL instance. A secret will be created with all the neccessary information to connect to the DB.

If you need further information on how to use OSBA with Kubernetes: <https://chrisdennig.me/2018/06/13/open-service-broker-for-azure-osba-with-azure-kubernetes-service-aks/>