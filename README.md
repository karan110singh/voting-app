# Project Description
This is a voting app project that allows users to vote for either cats or dogs. The votes are recorded in Redis and then read by a worker. The worker then sends that record to a Postgres database, and that record is reflected on the resulting app web page. The project uses Minikube.

# Requirements
1. Minikube
2. Docker

# Steps
Create pod.yml for all 5 services:
1.postgres-pod.yml
2. redis-pod.yml
3. voting-app-pod.yml
4. result-app-pod.yml
5. worker-app-pod.yml

Create service.yml for all 5 services:
1. postgres-service.yml
2. redis-service.yml
3. voting-app-service.yml
4. result-app-service.yml

# NOTE
Note that two of the services are web services (NodePort) and need to be connected from outside , while the other two services (ClusterIP) do not need to be connected internally.


