# kind-docker-image-automation

Builds and publishes multi-arch KinD node images for every Kubernetes releases.

## Workflows

- **k8s-repo-tag-sync** — Hourly sync of Kubernetes release tags from `kubernetes/kubernetes`. On new tags, triggers the build workflow.
- **build-kind-image** — Builds KinD node images (amd64 + arm64) for a given version tag and pushes them to ghcr.io (`kind-node` and `kind-node-ci`).

## Usage

Run "Build and push KinD node image" manually with a `tag` (e.g. `v1.30.0`). Or let the sync workflow run hourly to pick up new releases.
