# Installation 
## Add the Helm repository

```helm repo add kyverno https://kyverno.github.io/kyverno/```

## Scan your Helm repositories to fetch the latest available charts.
``` helm repo update ```
 
## Install the Kyverno Helm chart into a new namespace called "kyverno"

``` helm install kyverno --namespace kyverno kyverno/kyverno --create-namespace ```


# Policies

Under policies folder , there is a mutate policy that puts dockerhub.io imagepullsecret to containers pulling image except hb private image registries

``` kubectl create -f policies/mutate-imagepullsecret.yaml ```
