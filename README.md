# DevOps School Kubectl-AI

## Prompts examples for Kubernetes yaml manifests

| NAME             | PROMPT                                                                               | DESCRIPTION              | EXAMPLE                     |
|------------------|--------------------------------------------------------------------------------------|--------------------------|-----------------------------|
| app.yaml         | create pod "app" based on image gcr.io/k8s-k3s/demo:v1.0.0 with named http port 8000 | create pod app           | [app.yaml](./yaml/app.yaml) |
| app.yaml         | add labels app, run with value demo                                                  | add labels to app.yaml   | [app.yaml](./yaml/app.yaml) |
| app-livenessProbe.yaml | create pod "app-livenessprob" for liveness prob for app with timeoutSeconds, failureThreshold | create pod app-livenessProbe | [app-livenessProbe.yaml](./yaml/app-livenessProbe.yaml) |
| app-readinessProbe.yaml | create similar readiness probe with path /ready | create pod app-readinessProbe | [app-readinessProbe.yaml](./yaml/app-readinessProbe.yaml) |
| app-volumeMounts.yaml | create pod for app named "app-volume" with liveness probes like in app-livenessprob, readiness probes, and volume "data" with mount path /data and host path /var/lib/app | create pod app-volumeMounts | [app-volumeMounts.yaml](./yaml/app-volumeMounts.yaml) |
| app-cronjob.yaml | create CronJob scheduled every 5 minute and echo Hello world | create CronJob | [app-cronjob.yaml](./yaml/app-cronjob.yaml) |
| app-job.yaml | create Job "app-job-rsync" based on image google/cloud-sdk, command gsutil rsync, with volume mount path "/data/input" and pdName: glow-data-disk-200 | create rsync job | [app-job.yaml](./yaml/app-job.yaml) |
| app-multicontainer.yaml | create pod "app-multi-containers" with 2 containers: nginx, debian, and shared volume html, and command in debian container that write date to end of /html/index.html every 1 second | create multi-container pod | [app-multicontainer.yaml](./yaml/app-multicontainer.yaml) |
| app-resources.yaml | create pod "app-resource" based on gcr.io/kuar-demo/kuard-amd64:1, port 8080, with liveness probe /healthy, readiness probe /ready, requests resources cpu 100m, memory 128Mi and limits 256 Mi | create pod with resources limits | [app-resources.yaml](./yaml/app-resources.yaml) |
| app-secret-env.yaml | create pod "app-secret-env" with redis and secret env SECRET_USERNAME, SECRET_PASSWORD | create redis with secret envs | [app-secret-env.yaml](./yaml/app-secret-env.yaml) |
