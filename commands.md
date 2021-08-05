
## 1. Creating a job

```
$ fly -t tutorial login -c http://localhost:8080 -u test -p test

# use it also to update pipeline
$ fly -t tutorial set-pipeline -p hello-world -c hello-world.yml

# pipelines are paused when first created
$ fly -t tutorial unpause-pipeline -p hello-world

# trigger the job and watch it run to completion
$ fly -t tutorial trigger-job --job hello-world/hello-world-job --watch
```

## 2. Supplementary

### 2.1 Resources

> resources are distributed as Linux container images

```
# find out which resources a worker has
$ fly -t tutorial workers --details

bosh-io-release, bosh-io-stemcell, cf, docker-image, git, github-release, hg, mock, pool, registry-image, s3, semver, time, tracker
```

Resource source definitions:
- https://github.com/concourse/git-resource