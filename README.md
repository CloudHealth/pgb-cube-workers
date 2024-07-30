# pgb-cube-workers


The `pgb` deployment group specific repo extends the `cp-workers` repo's cube-worker deployment unit with containerization, and k8s deployment capabilities. This repo doesn't holds any application specific code. This fully re-uses the code base from cp-workers and this repo provides CI/CD enrichments to enable isolated testing


## sub-modules

To avoid code forking, cp-workers repo has been added as a sub-module. The entire cp-workers repo should be available under core-directory when you check-out this repo.

You can use the one of the following commands.

```sh
git clone https://github.com/CloudHealth/pgb-cube-workers.git
cd pgb-cube-workers
git submodule init
git submodule update
```

Alternatively you can also use this command

```sh
# haven't tested this yet, but expecting it to work.
git clone --recurse-submodules https://github.com/CloudHealth/pgb-cube-workers.git
```
