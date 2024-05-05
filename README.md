# DevOps School Kubectl-AI

## Prompts examples for Kubernetes yaml manifests

| NAME             | PROMPT                                                                               | DESCRIPTION              | EXAMPLE                     |
|------------------|--------------------------------------------------------------------------------------|--------------------------|-----------------------------|
| app.yaml         | create pod "app" based on image gcr.io/k8s-k3s/demo:v1.0.0 with named http port 8000 | create pod app           | [app.yaml](./yaml/app.yaml) |
| app.yaml         | add labels app, run with value demo                                                  | add labels to app.yaml   | [app.yaml](./yaml/app.yaml) |
| app-livenessProbe.yaml | create pod "app-livenessprob" for liveness prob for app with timeoutSeconds, failureThreshold | create pod app-livenessProbe | [app-livenessProbe.yaml](./yaml/app-livenessProbe.yaml) |
| app-readinessProbe.yaml | create similar readiness probe with path /ready | create pod app-readinessProbe | [app-readinessProbe.yaml](./yaml/app-readinessProbe.yaml) |
| app-volumeMounts.yaml | create pod for app named "app-volume" with liveness probes like in app-livenessprob, readiness probes, and volume "data" with mount path /data and host path /var/lib/app | create pod app-volumeMounts | [app-volumeMounts.yaml](./yaml/app-volumeMounts.yaml) |
