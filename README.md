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

Alternatively you can also use this command, once the changes are merged to prod

```sh
# haven't tested this yet, but expecting it to work.
git clone --recurse-submodules https://github.com/CloudHealth/pgb-cube-workers.git
```



## Running sub-module
This is very similar (if not same) to what you will do in cp-workers.

Step 1: Doing a bundle install.
```sh
rvm use ruby-2.5.5
rvm gemset use ruby-2.5.5@aws-digest-group --create
export USE_CHT_SRC=1
BUNDLE_GEMFILE=GemfileMriPgb PGB_GROUP_OVERRIDE=1 bundle install
```

Step 2: Running the rake
```sh
cd core

# VERIFY THAT WE'RE USING THE SAME GEMSET, BASED ON LOCAL SETUP AND IF WE DON'T USE RVM NEXT CMD IS NOT NEEDED
rvm gemset use ruby-2.5.5@aws-digest-group --create

# modify the above to choose the right rake task
BUNDLE_GEMFILE=../GemfileMriPgb PGB_GROUP_OVERRIDE=1 bundle exec rake 'partner:start'
```
