Flux v1 has reached **end of life** and has been replaced by [fluxcd/flux2](https://github.com/fluxcd/flux2)
and its controllers entirely.

If you consider using Flux, please take a look at <https://fluxcd.io/flux/get-started>
to get started with v2.

If you are on Flux Legacy, please follow the [migration guide](https://fluxcd.io/flux/migration).
If you need hands-on help migrating, you can contact one of the companies
[listed here](https://fluxcd.io/support/#my-employer-needs-additional-help).

<details>
  <summary>Flux v1 Helm repository</summary>

# Flux CD Helm repository

Add FluxCD repository to Helm repos:

```bash
helm repo add fluxcd https://charts.fluxcd.io
```

## Install Flux

```bash
helm upgrade -i flux fluxcd/flux \
--namespace fluxcd \
--set git.url=git@github.com:org/repo
```

For more details on installing Flux please see the [chart readme](https://github.com/fluxcd/flux/tree/master/chart/flux).

## Install Helm Operator

```bash
helm upgrade -i helm-operator fluxcd/helm-operator \
--namespace fluxcd \
--set git.ssh.secretName=flux-git-deploy \
--set createCRD=true
```

For more details on installing Flux Helm Operator please see the [chart readme](https://github.com/fluxcd/helm-operator/tree/master/chart/helm-operator).
</details>
