# gitops-pr-differ


## Builder gitops-pr-differ image

```bash
export VERSION=$(date +%Y%m%d%H%M)
export IMAGE="quay.io/openshift-examples/gitops-pr-differ:${VERSION}"
podman build --platform linux/amd64,linux/arm64  --manifest ${IMAGE}  .
podman manifest push ${IMAGE}
```