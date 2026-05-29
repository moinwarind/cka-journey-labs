# CKA Journey Labs

Hands-on Kubernetes labs from my CKA (Certified Kubernetes Administrator) preparation.

## What's here

- `Dockerfile` + `index.html` — first custom Docker image (Module 2)
- `web-app.yaml` — nginx Deployment with 3 replicas (Module 4)
- `web-svc.yaml` — NodePort Service exposing the Deployment
- `tester-pod.yaml` — Pod consuming ConfigMap via `envFrom`
- `shared-pod.yaml` — multi-container Pod sharing data via `emptyDir`
- `hostpath-pod.yaml` — Pod with `hostPath` volume (data survives Pod deletion)
- `yaml-lab/` — early YAML practice

Studying since May 2026. Target: CKA pass by August 2026.
