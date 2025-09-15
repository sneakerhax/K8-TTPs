# Containers

A list of vetted sources for exploiting, attacking, and escaping containers

## Exploits

* [Breaking out of Docker via runC – Explaining CVE-2019-5736](https://unit42.paloaltonetworks.com/breaking-docker-via-runc-explaining-cve-2019-5736/) - Yuval Avrahami (Palo Alto Networks)
* [Docker Patched the Most Severe Copy Vulnerability to Date With CVE-2019-14271](https://unit42.paloaltonetworks.com/docker-patched-the-most-severe-copy-vulnerability-to-date-with-cve-2019-14271/) - Yuval Avrahami (Palo Alto Networks)
* [CVE-2020-15275: New Vulnerability Exploits containerd-shim API](https://blog.aquasec.com/cve-2020-15257-containerd-shim-api-vulnerability) - Gal Singer (aquasec)
* [ABSTRACT SHIMMER (CVE-2020-15257): Host Networking is root-Equivalent, Again](https://www.nccgroup.com/us/research-blog/abstract-shimmer-cve-2020-15257-host-networking-is-root-equivalent-again/) - Jeff Dileo (NCC Group)
* [Using the Dirty Pipe vulnerability to break out from containers](https://www.datadoghq.com/blog/engineering/dirty-pipe-container-escape-poc/) - See post for authors (Datadog)
* [New Linux Vulnerability CVE-2022-0492 Affecting Cgroups: Can Containers Escape?](https://unit42.paloaltonetworks.com/cve-2022-0492-cgroups/) - Yuval Avrahami (Unit 42)
* [Leaky Vessels: runC and BuildKit container escape vulnerabilities - everything you need to know](https://www.wiz.io/blog/leaky-vessels-container-escape-vulnerabilities) - Merav Bar, Amitai Cohen, Itamar Gilad (Wiz)

## Attacking

* [Docker for Pentesters](https://blog.ropnop.com/docker-for-pentesters/) - ropnop
* [Serverless Toolkit for Pentesters](https://blog.ropnop.com/serverless-toolkit-for-pentesters/) - ropnop
* [Plundering Docker Images](https://blog.ropnop.com/plundering-docker-images/) - ropnop
* [Attacking Docker exposed API](https://medium.com/@riccardo.ancarani94/attacking-docker-exposed-api-3e01ffc3c124) - Riccardo Ancarani
* [Metasploit - Docker Daemon - Unprotected TCP Socket Exploit](https://www.rapid7.com/db/modules/exploit/linux/http/docker_daemon_tcp/) - Martin Pizala (Rapid7)
* [An Attacker Looks at Docker Approaching Multi Container Applications](https://youtu.be/-Ug2vmRiI8g) - Wesley McGrew
* [Docker image history modification - why you can't trust docker history](https://www.justinsteven.com/posts/2021/02/14/docker-image-history-modification/) - justinsteven
* [Watch Your Containers: Doki Infecting Docker Servers in the Cloud](https://www.intezer.com/blog/cloud-security/watch-your-containers-doki-infecting-docker-servers-in-the-cloud/) - Nicole Fishbein and Michael Kajiloti (Intezer)
* [PLAYING WITH NAMESPACES - WRITING DOCKER-AWARE ROOTKITS](https://pulsesecurity.co.nz/articles/docker-rootkits) - Denis Andzakovic (Pulse Security)

## Escapes

* [Understanding Docker container escapes](https://blog.trailofbits.com/2019/07/19/understanding-docker-container-escapes/) - Dominik Czarnota (Trail of Bits)
* [The Route to Root: Container Escape Using Kernel Exploitation](https://www.cyberark.com/resources/threat-research-blog/the-route-to-root-container-escape-using-kernel-exploitation) Nimrod Stoler (CyberArk)
* [A Compendium of Container Escapes](https://youtu.be/BQlqita2D2s) ([slides](https://i.blackhat.com/USA-19/Thursday/us-19-Edwards-Compendium-Of-Container-Escapes-up.pdf)) - Brandon Edwards & Nick Freeman
* [Docker - PRIVILEGE ESCALATION Technique](https://youtu.be/MnUtHSpcdLQ) - John Hammond
* [Bad Pods: Kubernetes Pod Privilege Escalation](https://bishopfox.com/blog/kubernetes-pod-privilege-escalation) - Seth Art (BishopFox)
* [Escaping Virtualized Containers](https://youtu.be/jFlqVe11eeM) - Yuval Avrahami
* [Root your Docker host in 10 seconds for fun and profit](https://www.electricmonk.nl/log/2017/09/30/root-your-docker-host-in-10-seconds-for-fun-and-profit/) - Ferry Boender
* [NVIDIAScape - Critical NVIDIA AI Vulnerability: A Three-Line Container Escape in NVIDIA Container Toolkit (CVE-2025-23266)](https://www.wiz.io/blog/nvidia-ai-vulnerability-cve-2025-23266-nvidiascape) - Nir Ohfeld, Shir Tamari
