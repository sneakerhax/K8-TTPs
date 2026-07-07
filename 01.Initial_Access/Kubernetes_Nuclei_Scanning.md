# Kubernetes Nuclei Scanning

**Description:** This entry describes how to scan Kubernetes for vulnerabilities using the open source tool Nuclei

**Requirements:** nuclei

**MSID:** MS-TA9004

## Scanning Kubernetes with Nuclei

```bash
nuclei -tags kubernetes -u <target-url>
```