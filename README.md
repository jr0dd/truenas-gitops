<div align="center">

I am no longer using TrueNAS SCALE. This has been archived as a point of reference for someone on TrueNAS SCALE to run with GitOps. 

</div>

---
## :book:&nbsp; Overview

This is home to my personal Kubernetes cluster. [Flux](https://github.com/fluxcd/flux2) watches this Git repository and makes the changes to my cluster based on the manifests in the [cluster](./cluster/) directory. [SOPS](https://toolkit.fluxcd.io/guides/mozilla-sops/) protects my secrets so I can keep everything on a public repo.

Currently I only have a single node with this running on TrueNAS SCALE. Which I am in the process of migrating to Ubuntu for all teh freedoms. If you use this repo to install on TrueNAS be prepared for some manual intervention since their middleware prevents certain system changes to persist updates and/or reboots. Please see the truenas.sh script in the [hack](./hack) directory. I disabled the bundled [openebs-zfs-localpv](https://github.com/openebs/zfs-localpv) so I had more freedom with updates by using the helm chart.


## Prometheus Rules
All my prometheus recording/alerting rules found in this repo can be found in my [prometheus-rules](https://github.com/jr0dd/prometheus-rules) repo.

## :handshake:&nbsp; Community

Thanks to all the people who donate their time to the [k8s@home](https://github.com/k8s-at-home/) community.
This repo would not exist if it wasn't for their work.

If you want to learn more start with this template [here](https://github.com/k8s-at-home/template-cluster-k3s/)
