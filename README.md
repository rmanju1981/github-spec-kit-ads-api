# github-spec-kit-ads-api

GitHub Spec Kit integration with Azure DevOps using Azure CLI OAuth (no PAT required).

## Included extension source

This repository now contains the source needed to use the Spec Kit Azure DevOps sync extension:

- `extension.yml` - Spec Kit extension manifest
- `commands/adosync.md` - command definition (`/speckit.azure-devops.sync`, alias `/speckit.adosync`)
- `scripts/bash/create-ado-workitems.sh` - Bash work-item sync script
- `scripts/powershell/create-ado-workitems.ps1` - PowerShell work-item sync script
- `config-template.json` - saved configuration template

## Install in Spec Kit

```bash
$env:SPECKIT_CATALOG_URL="https://raw.githubusercontent.com/github/spec-kit/main/extensions/catalog.community.json"
specify extension add azure-devops
```

## Prerequisites

- Azure CLI installed
- Azure DevOps CLI extension (`az extension add --name azure-devops`)
- Azure CLI login (`az login --use-device-code`)

## Usage

```text
/speckit.adosync
/speckit.adosync -FromTasks
```
