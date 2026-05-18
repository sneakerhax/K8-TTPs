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
| /openapi/v2                                            | OpenAPI v2 spec (full API schema) |
| /openapi/v3                                            | OpenAPI v3 spec (newer clusters) |
| /openapi.json                                          | OpenAPI schema (legacy alias) |
| /swagger.json                                          | Legacy Swagger spec      |
| /swagger-ui.html                                       | Swagger UI (if exposed)  |
| /healthz                                               | API server health check  |
| /livez                                                 | Liveness probe           |
| /readyz                                                | Readiness probe          |
| /metrics                                               | Prometheus metrics       |
| /logs                                                  | API server logs          |
| /api/v1/namespaces                                     | List all namespaces      |

## List of endpoints for the Kubelet API (Port: 10250)

| Endpoint       | Description                     |
|:---------------|:--------------------------------|
| /pods          | List pods running on the node   |
| /exec/<pod>    | RCE on pod                      |
| /run/<pod>     | Starts a new process in the pod |
| /logs/<pod>    | Review pod logs                 |
| /stats/summary | Detailed node resource usage    |
| /metrics       | Kubelet Prometheus metrics      |
| /healthz       | Kubelet health check            |
| /configz       | Kubelet runtime configuration   |
| /debug/pprof/  | Go profiling data (if enabled) |

## List of endpoints for ETCD API (Port: 2379)
| Endpoint                  | Description           |
|:--------------------------|:----------------------|
| /v2/keys/registry/secrets | Show all secrets      |
| /v2/keys/registry/pods    | List all pod details  |                     |
| /v2/keys/registry/nodes   | List all node details |
| /health                   | ETCD health check |
| /v2/members               | List ETCD cluster members |
| /v3/kv/range              | ETCD v3 key-value range query (gRPC-gateway) |

> **Note:** Most modern clusters use etcd v3; the /v2/ endpoints may not be available.

## List of endpoints for kube-proxy (Port: 10249)

| Endpoint | Description                     |
|:---------|:--------------------------------|
| /metrics | kube-proxy Prometheus metrics   |
| /healthz | Health check                    |

## List of endpoints for kube-scheduler (Port: 10259) and kube-controller-manager (Port: 10257)

| Endpoint | Description       |
|:---------|:------------------|
| /metrics | Component metrics |
| /healthz | Health check      |

## List of endpoints for the Metrics server

| Endpoint | Description              |
|:---------|:-------------------------|
| /healthz | Check API health         |
| /metrics | View API metrics         |
  
## References
* [Kubernetes Docs - The Kubernetes API](https://kubernetes.io/docs/concepts/overview/kubernetes-api/)
* [Kubernetes Docs - API Overview](https://kubernetes.io/docs/reference/using-api/)
* <a href="https://kubernetes.io/docs/reference/kubernetes-api/">Kubernetes API Reference</a>
* <a href="https://etcd.io/docs/v3.5/dev-guide/api_reference_v3/">ETCD v3 API</a>
* <a href="https://kubernetes.io/docs/reference/command-line-tools-reference/kubelet/">Kubelet API</a>
