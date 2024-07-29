# pgb-cube-workers

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
