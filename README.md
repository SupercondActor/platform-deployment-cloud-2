# SupercondActor Business Platform for Microsoft Azure Service Fabric
## Deployment scripts for remote Azure Service Fabric cluster

This repository contains scripts you can run to create new remote Azure Service Fabric cluster (or use an existing one) and deploy SupercondActor Business Platform into that cluster. The scripts also configure Azure Active Directory authentication for the cluster and the SupercondActor.

See detailed description at https://www.supercondactor.com/documentation

## Deployment to new cluster using ARM template

`src\CreateNewCluster_DeployApps_template.ps1`

This script creates new remote Azure Service Fabric cluster using ARM template `src\cluster.template.json`, configures Azure Active Directory authentication for the cluster, deploys SupercondActor applications and also configures Azure Active Directory authentication for the SupercondActor Service Manager UI.

## Deployment to new cluster using PowerShell command

`src\CreateNewCluster_DeployApps_script`

This script creates new remote Azure Service Fabric cluster using PowerShell command, installs cluster certificate into local certificate store to enable access to the cluster using Service Fabric Cluster Manager, deploys SupercondActor applications and also configures Azure Active Directory authentication for the SupercondActor Service Manager UI.

## Deployment to existing cluster using PowerShell command

`src\ExistingCluster_DeployApps_script.ps1`

This script installs existing cluster's certificate into local certificate store to enable access to the cluster using Service Fabric Cluster Manager, deploys SupercondActor applications and also configures Azure Active Directory authentication for the SupercondActor Service Manager UI.
