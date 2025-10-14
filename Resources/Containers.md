# Containers

A list of vetted sources for Red Teaming containers

## General

* [Docker for Pentesters](https://blog.ropnop.com/docker-for-pentesters/)
* [Serverless Toolkit for Pentesters](https://blog.ropnop.com/serverless-toolkit-for-pentesters/)
* [Plundering Docker Images](https://blog.ropnop.com/plundering-docker-images/)
* [An Attacker Looks at Docker Approaching Multi Container Applications](https://youtu.be/-Ug2vmRiI8g)
* [Docker image history modification - why you can't trust docker history](https://www.justinsteven.com/posts/2021/02/14/docker-image-history-modification/)

## Exploits

* [Docker: CVE-2016-9962: runC privilege escalation](https://www.rapid7.com/db/vulnerabilities/docker-cve-2016-9962/)
* [Breaking out of Docker via runC – Explaining CVE-2019-5736](https://unit42.paloaltonetworks.com/breaking-docker-via-runc-explaining-cve-2019-5736/) 
* [Docker Patched the Most Severe Copy Vulnerability to Date With CVE-2019-14271](https://unit42.paloaltonetworks.com/docker-patched-the-most-severe-copy-vulnerability-to-date-with-cve-2019-14271/)
* [CVE-2020-15275: New Vulnerability Exploits containerd-shim API](https://blog.aquasec.com/cve-2020-15257-containerd-shim-api-vulnerability)
* [ABSTRACT SHIMMER (CVE-2020-15257): Host Networking is root-Equivalent, Again](https://www.nccgroup.com/us/research-blog/abstract-shimmer-cve-2020-15257-host-networking-is-root-equivalent-again/)
* [Using the Dirty Pipe vulnerability to break out from containers](https://www.datadoghq.com/blog/engineering/dirty-pipe-container-escape-poc/)
* [New Linux Vulnerability CVE-2022-0492 Affecting Cgroups: Can Containers Escape?](https://unit42.paloaltonetworks.com/cve-2022-0492-cgroups/)
* [Leaky Vessels: runC and BuildKit container escape vulnerabilities - everything you need to know](https://www.wiz.io/blog/leaky-vessels-container-escape-vulnerabilities)
* [NVIDIAScape - Critical NVIDIA AI Vulnerability: A Three-Line Container Escape in NVIDIA Container Toolkit (CVE-2025-23266)](https://www.wiz.io/blog/nvidia-ai-vulnerability-cve-2025-23266-nvidiascape)

## Intial Access
* [Attacking Docker exposed API](https://medium.com/@riccardo.ancarani94/attacking-docker-exposed-api-3e01ffc3c124)
* [Metasploit - Docker Daemon - Unprotected TCP Socket Exploit](https://www.rapid7.com/db/modules/exploit/linux/http/docker_daemon_tcp/)


## Privilege Escalation

* [Understanding Docker container escapes](https://blog.trailofbits.com/2019/07/19/understanding-docker-container-escapes/)
* [The Route to Root: Container Escape Using Kernel Exploitation](https://www.cyberark.com/resources/threat-research-blog/the-route-to-root-container-escape-using-kernel-exploitation)
* [A Compendium of Container Escapes](https://youtu.be/BQlqita2D2s) ([slides](https://i.blackhat.com/USA-19/Thursday/us-19-Edwards-Compendium-Of-Container-Escapes-up.pdf))
* [Docker - PRIVILEGE ESCALATION Technique](https://youtu.be/MnUtHSpcdLQ)
* [Bad Pods: Kubernetes Pod Privilege Escalation](https://bishopfox.com/blog/kubernetes-pod-privilege-escalation)
* [Escaping Virtualized Containers](https://youtu.be/jFlqVe11eeM)
* [Root your Docker host in 10 seconds for fun and profit](https://www.electricmonk.nl/log/2017/09/30/root-your-docker-host-in-10-seconds-for-fun-and-profit/)
* [NVIDIAScape - Critical NVIDIA AI Vulnerability: A Three-Line Container Escape in NVIDIA Container Toolkit (CVE-2025-23266)](https://www.wiz.io/blog/nvidia-ai-vulnerability-cve-2025-23266-nvidiascape)

## Persistence

* [PLAYING WITH NAMESPACES - WRITING DOCKER-AWARE ROOTKITS](https://pulsesecurity.co.nz/articles/docker-rootkits)
* [Watch Your Containers: Doki Infecting Docker Servers in the Cloud](https://www.intezer.com/blog/cloud-security/watch-your-containers-doki-infecting-docker-servers-in-the-cloud/)
* [Intro to Fileless Malware in Containers](https://www.aquasec.com/blog/intro-to-fileless-malware-in-containers/)
* [Fileless malware mitigation](https://www.sysdig.com/blog/containers-read-only-fileless-malware)
