# pre-commit-kustomize

## Example

```yaml
# See https://pre-commit.com for more information
repos:
-   repo: https://github.com/dsch/pre-commit-kustomize
    rev: master
    hooks:
    -   id: kustomize
        name: kustomize-development
        args: [overlays/production]
        files: [overlays/production]
    -   id: kustomize
        name: kustomize-development
        args: [overlays/development]
        files: [overlays/development]
