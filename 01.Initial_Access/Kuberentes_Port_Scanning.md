# Kubernetes Port Scanning

**Description:** This entry describes how to scan Kubernetes clusters for exposed ports

**Requirements:** nmap

**Optional:** docker

**MSID:** MS-TA9005

## List of Kubernetes and related service ports
| Name                         | Port/Protocol   | Service        | Availability |
|:-----------------------------|:----------------|:---------------|:-------------|
| CoreDNS                      | 53/tcp          | DNS            | Internal     |
| Kubernetes HTTP              | 80/tcp          | HTTP           | External     |
| Calico BGP                   | 179/tcp         | BGP            | Internal     |
| Kubernetes HTTPS             | 443/tcp         | HTTPS          | External     |
| CoreDNS Metrics              | 9153/tcp        | HTTP           | Internal     |
| Docker daemon                | 2375/tcp        | Docker API     | Internal     |
| Docker daemon TLS            | 2376/tcp        | Docker API TLS | Internal     |
| etcd client                  | 2379/tcp        | etcd client    | Internal     |
| etcd peer                    | 2380/tcp        | etcd peer      | Internal     |
| etc metrics.                 | 2381/tcp        | etcd metrics.  | Internal     |
| Argo Workflows               | 2746/tcp        | HTTP           | Internal     |
| Grafana                      | 3000/tcp        | HTTP           | Mixed        |
| Weave Scope                  | 4040/tcp        | HTTP           | Internal     |
| cAdvisor legacy              | 4194/tcp        | Metrics        | Internal     |
| Registry proxy HTTP          | 5000/tcp        | HTTP           | Internal     |
| Registry proxy HTTPS         | 5001/tcp        | HTTPS          | Internal     |
| K8s API server               | 6443/tcp        | HTTPS          | Mixed        |
| Weave Net data               | 6783/tcp        | Weave mesh     | Internal     |
| Weave Net control            | 6784/tcp        | Weave ctl      | Localhost    |
| Cluster gossip               | 7946/tcp        | Gossip         | Internal     |
| K8s dashboard                | 8001/tcp        | HTTP           | Internal     |
| API, KubeProxy, Kubeflow     | 8080/tcp        | HTTP           | Mixed        |
| NGINX ingress, Apache NiFi   | 8443/tcp        | HTTPS          | External     |
| Prometheus                   | 9090/tcp        | HTTP           | Internal     |
| Alertmanager                 | 9093/tcp        | HTTP           | Internal     |
| calico-felix health          | 9099/tcp        | Health         | Internal     |
| Node exporter                | 9100/tcp        | Metrics        | Internal     |
| Docker metrics               | 9323/tcp        | Metrics        | Internal     |
| Webhooks/controllers         | 9443/tcp        | HTTPS          | Internal     |
| kube-proxy metrics           | 10249/tcp       | Metrics        | Internal     |
| kubelet API                  | 10250/tcp       | Kubelet API    | Internal     |
| kube-scheduler               | 10251/tcp.      | HTTP           | Internal     |
| kube-controller-manager      | 10252/tcp       | HTTP           | Internal     |
| kubelet read-only            | 10255/tcp       | Read-only API  | Internal     |
| kube-proxy                   | 10256/tcp       | Health         | Internal     |
| controller-manager           | 10257/tcp       | HTTPS          | Internal     |
| scheduler                    | 10259/tcp       | HTTPS          | Internal     |
| Envoy admin                  | 15000/tcp       | Admin API      | Internal     |
| Istio status                 | 15020/tcp       | Status         | Internal     |
| Istio health                 | 15021/tcp       | Health         | Internal     |
| Envoy metrics                | 15090/tcp       | Metrics        | Internal     |
| NodePort                     | 30000-32767/tcp | Varies         | External     |

### UDP discovery ports
| Name             | Port/Protocol   | Service    | Availability |
|:-----------------|:----------------|:-----------|:-------------|
| CoreDNS          | 53/udp          | DNS        | Interal      |
| VXLAN overlay    | 4789/udp        | VXLAN      | Internal     |
| Weave Net data   | 6783/udp        | Weave mesh | Internal     |
| Weave Net control| 6784/udp        | Weave ctl  | Internal     |
| Cluster gossip   | 7946/udp        | Gossip     | Internal     |
| Flannel VXLAN    | 8472/udp        | VXLAN      | Internal     |
| NodePort         | 30000-32767/udp |            | External     |

## Scanning for exposed TCP ports in Kubernetes using Nmap

```bash
nmap -Pn --open --reason -sV --script=http-title -p 53,80,179,443,9153,2375,2376,2379,2380,2381,2746,3000,4040,4194,5000,5001,6443,6783,6784,7946,8001,8080,8443,9090,9093,9099,9100,9323,9443,10249,10250,10251,10252,10255,10256,10257,10259,15000,15020,15021,15090,30000-32767 <target>
```

Scanning Kubernetes TCP services using the ports listed in the above table.


```bash
docker run --rm --entrypoint nmap sneakerhax/nmap -Pn --open --reason -sV --script=http-title -p 53,80,179,443,9153,2375,2376,2379,2380,2381,2746,3000,4040,4194,5000,5001,6443,6783,6784,7946,8001,8080,8443,9090,9093,9099,9100,9323,9443,10249,10250,10251,10252,10255,10256,10257,10259,15000,15020,15021,15090,30000-32767 <target>
```

Scanning Kubernetes TCP services with the Docker container sneakerhax/nmap

### Scanning for exposed UDP ports in Kubernetes using Nmap

```bash
docker run --rm --entrypoint nmap sneakerhax/nmap -Pn --open --reason -sU --version-light -p 53,4789,6783,6784,7946,8472,30000-32767 <target>
```

Scanning Kubernetes UDP services using the ports listed in the above table.

```bash
docker run --rm --entrypoint nmap sneakerhax/nmap -Pn --open --reason -sU --version-light -p 53,4789,6783,6784,7946,8472,30000-32767 <target>
```

Scanning Kubernetes UDP services with the Docker container sneakerhax/nmap
  
## References
* [Kubernetes Docs - Ports and Protocols](https://kubernetes.io/docs/reference/networking/ports-and-protocols/)
