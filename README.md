# abs-kubernetes

Dockerfile:

This setup will use the nginx official docker image as base image
and Copies all the html files to nginx root folder: /usr/share/nginx/html/

and After Building and pushing the Docker image to the target registry i.e. Docker registry or Azure container registry.

Helm charts:

Helm charts contains basic deployment.yaml and service.yaml templates which will help to deploy the docker image on to the targetted Kubernetes server or AKS.
Values.yml contains the basic details like registry address and port number etc.

Deloyment file referrs to image pull secret which will already be stored on AKS with credentials for the docker image source registry.

Kubernetes:

this setup was built and tested on Azure kubernetes service cluster.
we can even use any kubernetes services provided by any cloud provider or local cluster built by minikube etc.