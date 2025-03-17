# Kubernetes Port Scanning

**Description:** This entry describes how to scan Kubernetes clusters for exposed ports

**Requirements:** nmap

**MSID:** MS-TA9005

## List of ports
| Name                                             | Port/Protocol   |
|--------------------------------------------------|-----------------|
| http Kubernetes                                  | 80/tcp          |
| https Kubernetes                                 | 443/tcp         |
| etcd service                                     | 2379/tcp        | 
| Argo Workflows                                   | 2746/tcp        | 
| Weave Scope                                      | 4040/tcp        |  
| kubelet (cAdvisor)                               | 4149/tcp        | 
| http kube-registry-proxy                         | 5000/tcp        |
| https kube-registry-proxy                        | 5001/tcp        |
| Kubernetes API server                            | 6443/tcp        | 
| Kubernetes dashboard                             | 8001/tcp        | 
| Kubeflow                                         | 8080/tcp        |
| Kubernetes Nginx ingress controller, Apache NiFi | 8443/tcp        | 
| calico-felix health check server                 | 9099/tcp        | 
| kubelet API full node access                     | 10250/tcp       |
| kubelet Unauthenticated read-only port           | 10255/tcp       | 
| kube-proxy                                       | 10256/tcp       | 
|  NodePort                                        | 30000-32767/tcp |

## Scanning for exposed ports in Kubernetes using Nmap

```
nmap -Pn --open -sV --script=http-title -p 80,443,4040,4149,5000,5001,6443,8001,8080,8443,9099,10250,10255,10256,30000-32767
```

Command explanation
  
## References
* [Kubernetes Docs - Ports and Protocols](https://kubernetes.io/docs/reference/networking/ports-and-protocols/)
