## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

  helm repo add <alias> https://thecyberdock.github.io/thecyberdock-app/  

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
<alias>` to see the charts.

To install the cyberdock chart:

    helm install cyberdock <alias>/cyberdock

To uninstall the chart:

    helm delete cyberdock

  
 
Minimal values.yml file
  
  
```yml
namespace: cyberdock

cyberdock:
  nodePort: 31525
  image: thecyberdock/thecyberdock-app
  tag: latest
  SECRET_KEY: example
  REDIS_URL: redis://example/redis
  ELASTIC_URL: https://elastic.example.com/
  DATABASE_URL:  postgres://example:example/db


```
