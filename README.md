# shack-gitops

The **YAML repo** for the DevOps Shack App of Apps lab. Argo CD reads only this repo.

- `argocd/root.yaml` – the root Application. Apply it once with kubectl.
- `argocd-apps/` – everything the root app manages: one AppProject and one Application per app.
- `apps/` – the Kubernetes YAML for each app. `apps/shack-app/kustomization.yaml` holds the image tag that GitHub Actions in the **shack-app** repo updates on every build.
- `extras/` – an app you add during the demo by moving its file into `argocd-apps/`.

Sync waves: project (-2) → cache (0) → shack-app (1) → web (2) → tools (3).
