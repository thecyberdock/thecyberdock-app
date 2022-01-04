## About

### [Cyberdock](https://thecyberdock.com/)

Automating Kubernetes & OpenShift security controls for mission-critical environments

For any questions or feedback [Contact Us](mailto:welcome@thecyberdock.com)

## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

``` sh

  helm repo add cyberdock https://thecyberdock.github.io/thecyberdock-app/  
```

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
<alias>` to see the charts.

To install the cyberdock chart:

    helm install cyberdock cyberdock/cyberdock --create-namespace -n cyberdock

To uninstall the chart:

    helm delete cyberdock

To upgrade when new version is available:

```
helm upgrade cyberdock cyberdock/cyberdock
```
#### Open shift instructions

1. Create new project 

```
oc new-project cyberdock
```

2. Add helm repo

```
  helm repo add <alias> https://thecyberdock.github.io/thecyberdock-app/  
```

3. Update repo

```
helm repo update
```

4. Install 

```
 helm install cyberdock <alias>/cyberdock
```



Web UI would be available on the Node port specified in the configuration

By default only 1 replica is deployed
