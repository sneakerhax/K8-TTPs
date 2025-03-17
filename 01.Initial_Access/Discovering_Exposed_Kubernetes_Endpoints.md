# Discovering Exposed Kubernetes Endpoints

**Description:** This entry describes endpoints you can check to verify access to Kubernetes

**Requirements:** browser, curl

**MSID:** MS-TA9005

## Checking for endpoint exposure

```
curl -ILk https://kubernetes.server.api:<port>/<endpoint>
```

Check for endpoint exposure using curl

## List of endpoints for the K8s API server (Port: 80, 443, 6443)

| Endpoint                                               | Description              |
|:-------------------------------------------------------|:-------------------------|
| /version                                               | Check the API version    |
| /api                                                   | List api version         |
| /apis                                                  | List available resources |
| /api/v1/nodes                                          | List node information    |
| /api/v1/pods                                           | List pod information     |
| /api/v1/secrets                                        | List secrets             |
| /api/v1/configmaps                                     | List configmaps          | 
| /api/v1/serviceaccounts/token                          | Show servicetoken        |
| /apis/authorization.k8s.io/v1/selfsubjectaccessreviews | Check user permission    |
| /apis/autoscaling/v1/horizontalpodautoscalers          | List scaling policies    |

## List of endpoints for the Kubelet API (Port: 10250)

| Endpoint       | Description                     |
|:---------------|:--------------------------------|
| /pods          | List pods running on the node   |
| /exec/<pod>    | RCE on pod                      |
| /run/<pod>     | Starts a new process in the pod |
| /logs/<pod>    | Review pod logs                 |
| /stats/summary | Detailed node resource usage    |

## List of endpoints for ETCD API (Port: 2379)
| Endpoint                  | Description           |
|:--------------------------|:----------------------|
| /v2/keys/registry/secrets | Show all secrets      |
| /v2/keys/registry/pods    | List all pod details  |                     |
| /v2/keys/registry/nodes   | List all node details |

## List of endpoints for the Metrics server

| Endpoint | Description              |
|:---------|:-------------------------|
| /healthz | Check API health         |
| /metrics | View API metrics         |
  
## References
* [Kubernetes Docs - The Kubernetes API](https://kubernetes.io/docs/concepts/overview/kubernetes-api/)
* [Kubernetes Docs - API Overview](https://kubernetes.io/docs/reference/using-api/)
