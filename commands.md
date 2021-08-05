

```
$ fly -t tutorial login -c http://localhost:8080 -u test -p test

# use it also to update pipeline
$ fly -t tutorial set-pipeline -p hello-world -c hello-world.yml

# pipelines are paused when first created
$ fly -t tutorial unpause-pipeline -p hello-world

# trigger the job and watch it run to completion
$ fly -t tutorial trigger-job --job hello-world/hello-world-job --watch
```