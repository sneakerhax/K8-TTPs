# Kubernetes Port Scanning

**Description:** This entry describes how to scan Kubernetes clusters for exposed ports

**Requirements:** nmap

**MSID:** MS-TA9005

## Section

```
nmap -Pn --open -sV --script=http-title -p 80,443,4040,4149,5000,5001,6443,8001,8080,8443,9099,10250,10255,10256,30000-32767
```

Command explanation
  
## References
* [Kubernetes Docs - Ports and Protocols](https://kubernetes.io/docs/reference/networking/ports-and-protocols/)
