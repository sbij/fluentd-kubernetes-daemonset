# Fluentd Daemonset for Kubernetes

## Standalone version
For using Fluentd on the same machine than the Elasticsearch instance, you should use the **standalone** version `docker-image/v0.12/debian-fluentd-standalone`.
Then you can use the DockerHub link in the Kubernetes charts to launch the full architecture (see repository [sbij/kubernetes-logging-charts](https://github.com/sbij/kubernetes-logging-charts)).


## Normal version
For using Fluentd as a normal daemonset, which will send the logs to a remote Fluentd instance though an ip, use the **normal** version `docker-image/v0.12/debian-fluentd`.

Then you can launch the daemonset with: `kubectl create -f fluentd-daemonset-elasticsearch.yaml`.

## Building the DockerHub image
In the folder:
```
docker build -t username/repository .
docker login
docker push username/repository:tag
```

