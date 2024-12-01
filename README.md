Cosmocloud Deploy Helm Chart
============================

Overview
--------

this repo contains a helm chart to deploy a simple 3 tier application 

This Helm chart deploys a complete application stack with:

-   1 Backend Service
-   1 Frontend Service
-   1 Redis Database

Prerequisites
-------------

-   Kubernetes Cluster
-   Helm 3.x
-   kubectl

Deployment
----------

To deploy the application:

`
helm install testapp cosmocloud-deploy --atomic --timeout 30s
`

Configuration
-------------

Modify `values.yaml` to customize:

-   Image versions
-   Replica counts
-   Environment variables

Services
--------

1.  Backend Service (ClusterIP)
    -   Name: backend-svc
    -   Port: 8000
2.  Frontend Service (NodePort)
    -   Name: frontend-svc
    -   Port: 5175
    -   NodePort: 31000
3.  Redis Service (ClusterIP)
    -   Name: redis-svc
    -   Port: 6379
