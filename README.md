# pre-commit-kustomize

## Example

```yaml
# See https://pre-commit.com for more information
repos:
  - repo: https://github.com/dsch/pre-commit-kustomize
    rev: v1.0.0
    hooks:
      - id: kustomize
        name: kustomize-development
        args: [ overlays/production ]
        files: ^overlays/production
      - id: kustomize
        name: kustomize-development
        args: [ overlays/development ]
        files: ^overlays/development
```

## Specify kustomize version

```yaml
repos:
  - repo: https://github.com/dsch/pre-commit-kustomize
    rev: v1.0.0
    hooks:
      - id: kustomize
        name: kustomize-development
        entry: --entrypoint /app/kustomize k8s.gcr.io/kustomize/kustomize:v4.3.0 build
        args: [ overlays/production ]
        files: ^overlays/production
```
