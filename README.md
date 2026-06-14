# CKA Journey Labs

Hands-on Kubernetes labs from my path to the **Certified Kubernetes Administrator (CKA)** exam.
Everything here is built and tested on a local single-node cluster (Docker Desktop, macOS).

**Target: CKA pass by August 2026** · Studying since May 2026

---

## Why this repo

I'm an IT professional transitioning toward Platform/DevOps. Rather than just watch
courses, I build and break things — every concept here is something I've applied
on a live cluster, not just read about. The YAML workflow throughout uses
`kubectl ... --dry-run=client -o yaml` as the base, then edited by hand.

## Environment

- macOS · Docker Desktop · single-node Kubernetes
- `kubectl` with aliases + speed drills for exam pace

## What's covered

**Workloads & config**
- `web-app.yaml` — nginx Deployment, 3 replicas
- `web-svc.yaml` — NodePort Service exposing the Deployment
- `tester-pod.yaml` — Pod consuming a ConfigMap via `envFrom`
- `hello-job.yaml` / `hello-cronjob.yaml` — Jobs and CronJobs

**Storage**
- `my-pv.yaml` / `my-pvc.yaml` / `pv-pod.yaml` — PersistentVolume → PVC → Pod
- `hostpath-pod.yaml` — hostPath volume (data survives Pod deletion)
- `shared-pod.yaml` — multi-container Pod sharing data via `emptyDir`

**RBAC**
- `pod-reader-role.yaml` / `pod-reader-binding.yaml` — namespaced Role + RoleBinding
- `node-reader-clusterrole.yaml` / `node-reader-clusterrolebinding.yaml` — cluster-scoped access

**Networking**
- `deny-all-ingress.yaml` — default-deny NetworkPolicy

**Troubleshooting**
- `broken-pod-1.yaml` / `broken-pod-2.yaml` — deliberately broken Pods to diagnose and fix
- `scenario3-deploy.yaml` / `scenario3-svc.yaml` — debugging a Deployment + Service end to end

**Containers (foundation)**
- `Dockerfile` + `index.html` — first custom image, then deployed to the cluster

## Progress

- [x] Module 1–2 — Containers, Docker, first images
- [x] Module 3 — Pods, ReplicaSets, Deployments
- [x] Module 4 — Volumes, PV/PVC, StatefulSets, DaemonSets, Jobs, RBAC, NetworkPolicy, troubleshooting
- [ ] Module 5 — kubectl speed drills, exam-pace practice *(in progress)*
- [ ] Mock exams

---

*Updated as I go. Feedback welcome.*
