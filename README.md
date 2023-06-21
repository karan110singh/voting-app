Project Description
This is a voting app project that allows users to vote for either cats or dogs. The votes are recorded in Redis and then read by a worker. The worker then sends that record to a Postgres database, and that record is reflected on the resulting app web page. The project uses Minikube.

Requirements
Minikube
Docker

# Steps
Create pod.yml for all 5 services:
postgres-pod.yml
redis-pod.yml
voting-app-pod.yml
result-app-pod.yml
worker-app-pod.yml

Create service.yml for all 5 services:
postgres-service.yml
redis-service.yml
voting-app-service.yml
result-app-service.yml

# NOTE
Note that two of the services are web services (NodePort) and need to be connected from outside , while the other two services (ClusterIP) do not need to be connected internally.


