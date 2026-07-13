# Discovering Kubernetes secrets in GitHub repos with Trufflehog

**Description:** This entry describes how to discover Kubernetes related secrets with Trufflehog in GitHub repos

**Requirements:** trufflehog

**Optional:** docker

**MSID:** MS-TA9001, MS-TA9003

## Scan GitHub org for secrets

```
trufflehog github --org=org_name
```

Scanning a GitHub org for secrets.

## Scan GitHub org for secrets (Verified only)

```
trufflehog github --org=org_name --results=verified
```

Scanning a GitHub org for secrets that are verified.

## Scanning a GitHub org for secrets with Docker

```
docker run --rm -it trufflesecurity/trufflehog github --org=org_name
```

Scanning a GitHub org for secrets using Docker

## Scanning a GitHub repo

```
trufflehog github --repo=https://github.com/org/repo
```

Scanning a GitHub repo for secrets. Additional arguments available for scanning pull request and issue comments.

## References
* [GitHub - Trufflehog](https://github.com/trufflesecurity/trufflehog)
* [Trufflehog - Docs](https://trufflesecurity.com/docs)
